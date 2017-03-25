## Phalcon 3.1.1 released!

Hey everyone.

We are releasing a hotfix today 3.1.1 that addresses some urgent issues with the framework. We strongly recommend that you upgrade your Phalcon version to the latest release 3.1.1.

As with any software, we have the `you broke it` scenario here. Thanks to the quick reporting from the community, we managed to fix the issues that came up, and therefore issue the hotfix today.

The release tag can be found here: [3.1.1](https://github.com/phalcon/cphalcon/releases/tag/v3.1.1)

### Undefined indexes in models
After the upgrade to 3.1.0, all models were issuing warnings:

```
Undefined index: keepSnapshots in Users.php on line 61
Undefined index: keepSnapshots in Groups.php on line 57
```

The issue would be rectified after clearing the query cache but still not a perfect solution. We have fixed it with [PR-12737](https://github.com/phalcon/cphalcon/pull/12737).

### `doLowUpdate()` - First argument is not array
After the upgrade we have experienced the following issue:

```php
$robot = Robots::findFirst();

$robot2 = new Robot($robot->toArray(), $di, $modelsManager);
$robot2->setNewValueForField(100);

try {
    $robot2->setDirtyState($robot2::DIRTY_STATE_PERSISTENT); 
    $robot2->save();
} catch (\Exception $exception) {
   echo "ERROR: " . $exception->getMessage();
}
Results in:
ERROR: First argument is not an array
```

It was reported in [#12742](https://github.com/phalcon/cphalcon/issues/12742) and it was fixed with [PR-12739](https://github.com/phalcon/cphalcon/pull/12739).

### Expanding on 3.1.0 Version highlights

- ##### Added `Phalcon\Validation\Validator\Callback`, `Phalcon\Validation::getData` [NEW]
  We added new validator `Phalcon\Validation\Validator\Callback` where you can execute any logic you want. It should return `true`, `false` 
  or new Validator which should be used to validate your field.
  
  ```php
  <?php
  
  use Phalcon\Validation;
  use Phalcon\Validation\Validator\Callback;
  use Phalcon\Validation\Validator\PresenceOf;
  
  $validation = new Validation();
  $validation->add(
      "amount",
      new Callback(
          [
              "callback" => function($data) {
                  return $data["amount"] % 2 == 0;
              },
              "message" => "Only even number of products are accepted"
          ]
      )
  );
  
  $messages = $validation->validate(["amount" => 1]); // will return message from first validator
  ```
  
  For more information read [docs reference](https://docs.phalconphp.com/en/latest/reference/validation.html#callback-validator)
- Added the ability to truncate database tables
- ##### Added `Phalcon\Mvc\Model\Binder`, class used for binding models to parameters in dispatcher, micro, added `Phalcon\Dispatcher::getBoundModels` and `Phalcon\Mvc\Micro::getBoundModels` to getting bound models, added `Phalcon\Mvc\Micro\Collection\LazyLoader::callMethod`
  In Phalcon 3 we introduced binding model instances in controller actions. In Phalcon 3.1 we decided to move code which is doing it
  to separated class, optimize it a bit and add way to use same functionality in `Phalcon\Mvc\Micro` as well. Since it's
  using Reflection API we also added way to cache it.
  
  In addition to this `Phalcon\Dispatcher::setModelBinding()` is now deprecated and will be removed in Phalcon 4. From Phalcon 3.2 usage of
  this method will trigger `E_DEPRECATED`
  
  ```php
  <?php

  use Phalcon\Di\FactoryDefault;
  use Phalcon\Mvc\Dispatcher;
  use Phalcon\Mvc\Model\Binder;

  $di = new FactoryDefault();
  $di->set('dispatcher', function() {
      $dispatcher = new Dispatcher();
      $dispatcher->setModelBinder(new Binder(), 'cache');
      return $dispatcher;
  });
  ```
  
  And you can type-hint your action parameters with class names. For more information read docs:
  - [using in micro](https://docs.phalconphp.com/en/latest/reference/micro.html#inject-model-instances)
  - [using in dispatcher](https://docs.phalconphp.com/en/latest/reference/dispatching.html#inject-model-instances)
- ##### Added `afterBinding` event to `Phalcon\Dispatcher` and `Phalcon\Mvc\Micro`, added `Phalcon\Mvc\Micro::afterBinding` [NEW]
  We added new event to dispatcher and micro application. `afterBinding` event(or middleware in micro) will happen after binding model instances
  done by component `Phalcon\Mvc\Model\Binder` but before executing an action.
- ##### Added the ability to set custom Resultset class returned by `find()` [#12166](https://github.com/phalcon/cphalcon/issues/12166) [NEW]
  By using this feature you can have your own custom Resultset classes with your own logic.
  
  ```php
  <?php

  use Phalcon\Mvc\Model;
  use Phalcon\Mvc\Model\Resultset\Simple;

  class AgeStats extends Model
  {
      public function getSource()
      {
          return 'stats';
      }
      public function getResultsetClass()
      {
          return 'MyResultset';
      }
  }

  class MyResultset extends Simple 
  {
     // implement your custom logic here
  }

  $stats = AgeStats::find(); // it will return MyResultset instance
  ```
- ##### Clear appended and prepended title elements (`Phalcon\Tag::appendTitle`, `Phalcon\Tag::prependTitle`) [NEW]
  You can now clear and add multiple elements to `appendTitle` and `prependTitle` on the `Phalcon\Tag` component.

  ```php
  <?php
  A way to clear elements and to add multiple elements at once (why not)  .
  \Phalcon\Tag::setTitleSeparator(' - ');
  \Phalcon\Tag::setTitle('Title');
  
  // Somewhere in controller
  \Phalcon\Tag::prependTitle('Category');
  \Phalcon\Tag::prependTitle('Article');
  
  // Same situation - clear and put just one prepend element (will be faster than clear all values)
  \Phalcon\Tag::prependTitle(['Just article']);
  
  // Or other - clear and put a few elements
  \Phalcon\Tag::prependTitle(['Other category', 'Other article']);
  ```

- ##### Added the ability to specify what empty means in the `'allowEmpty'` option of the validators. Now it accepts as well an array specifying what's empty, for example `['', false]` [NEW]
  Previously `allowEmpty` option in validators would accept only true value, meaning it allows empty values. Right now you can
  provide what exactly values are accepted as empty as an array.
  
  ```php
  <?php

  use Phalcon\Validation;
  use Phalcon\Validation\Validator\PresenceOf;

  $validation = new Validation();
  $validation->add('description', new PresenceOf(
      [
          'message' => 'Description is required',
          'allowEmpty' => [null]
      ]
  ));

  $messages = $validation->validate(['description' => null]); // empty messages
  $messages = $validation->validate(['description' => '']); // will return message from validator
  ```
- ##### Added the ability to use `Phalcon\Validation` with `Phalcon\Mvc\Collection`, deprecated `Phalcon\Mvc\Model\Validator` classes [NEW]
  In Phalcon 3 we made change to model validations that it's using the same validation classes as forms. But the similar change
  was missing for `Phalcon\Mvc\Collection`. Right now we changed it and you can use `Phalcon\Validation` component for Mongo Collections.
  The required changes were also made for [phlacon/incubator](https://github.com/phalcon/incubator) and PHP7 related classes.
  
  We encourage you to switch to new validation, in Phalcon 4 we will remove old `Phalcon\Mvc\Model\Validator` namespace.
  From Phalcon 3.2 usage of old classes will trigger `E_DEPRECATED`
  
  ```php
  <?php

  use Phalcon\Mvc\Collection;
  use Phalcon\Validation;
  use Phalcon\Validation\Validator\PresenceOf;

  class Robots extends Collection
  {
      public function validation()
      {
          $validation = new Validation();
          $validation->add('name', new PresenceOf());
          return $this->validate($validation);
      }
  }

  $robots = new Robots();
  $robots->create(); // returns false
  $robots->name = 'Some Robot';
  $robots->create(); // returns true
  ```
  
  For more information read docs:
  - [validating collections](https://docs.phalconphp.com/pl/latest/reference/odm.html#validating-data-integrity)
  - [validation](https://docs.phalconphp.com/en/latest/reference/validation.html)
- Added the value of the object `instanceof` Interface to `Phalcon\Acl\Adapter\Memory`
- Added the ability to get original values from `Phalcon\Mvc\Model\Binder`, added `Phalcon\Mvc\Micro::getModelBinder`, `Phalcon\Dispatcher::getModelBinder`
- Added `prepend` parameter to `Phalcon\Loader::register` to specify autoloader's loading order to top most
- Fixes internal cache saving in `Phalcon\Mvc\Model\Binder` when no cache backend is used
- Fixed `Phalcon\Session\Bag::remove` to initialize the bag before removing a value [#12647](https://github.com/phalcon/cphalcon/pull/12647)
- Fixed `Phalcon\Mvc\Model::getChangedFields` to correct detect changes from `NULL` to Zero [#12628](https://github.com/phalcon/cphalcon/issues/12628)
- Fixed `Phalcon\Mvc\Model` to create/refresh snapshot after create/update/refresh operation [#11007](https://github.com/phalcon/cphalcon/issues/11007), [#11818](https://github.com/phalcon/cphalcon/issues/11818), [#11424](https://github.com/phalcon/cphalcon/issues/11424)
- Fixed `Phalcon\Mvc\Model::validate` to correctly set code message [#12645](https://github.com/phalcon/cphalcon/issues/12645)
- Fixed `Phalcon\Mvc\Model` to correctly add error when try to save empty string value to not null and not default column [#12688](https://github.com/phalcon/cphalcon/issues/12688)
- Fixed `Phalcon\Validation\Validator\Uniqueness` collection persistent condition
- Fixed `Phalcon\Loader::autoLoad` to prevent PHP warning [#12684](https://github.com/phalcon/cphalcon/pull/12684)
- Fixed `Phalcon\Mvc\Model\Query::_executeSelect` to correctly get the column map [#12715](https://github.com/phalcon/cphalcon/issues/12715)
- Fixed params view scope for PHP 5 [#12648](https://github.com/phalcon/cphalcon/issues/12648)
			
##### Please note that Phalcon 3.1 is not compatible with PHP 7.1. If you want to use PHP 7, you will need to compile it with PHP 7.0. Full support for PHP 7.1+ will be introduced in our next version ##### {.alert .alert-danger}

### Community 
Big kudos to our community as always for reporting, suggesting and applying fixes and making our framework better with every release! A big thank you to all our backers and supporters that help us by joining our funding campaign. [https://phalcon.link/fund](https://phalcon.link/fund)

### Team
We are making some changes to our team, bringing more people in to help with the organization, management as well as structure of the project. Our end goals are to produce timely releases with zero or minimal bugs, and to implement new features regularly. This is still work in progress, so once we have everything settled, we will explain everything with a relevant blog post.

### Update/Upgrade

Phalcon 3.1.0 can be installed from the `master` branch, if you don't have Zephir installed follow these instructions:

```sh
git clone http://github.com/phalcon/cphalcon
cd cphalcon/build
sudo ./install
```

Note that running the installation script will replace any version of Phalcon installed before.

[PackageCloud.io](https://packagecloud.io/phalcon/stable) has been updated to allow your package manager (for Linux machines) to upgrade to the new version seamlessly.

Windows DLLs are available in the [download page](https://phalconphp.com/en/download/windows).

##### Linux packages will be available in a couple of hours after the posting of this blog post ##### {.alert .alert-info}



We encourage existing Phalcon 3 users to update to this version.


<3 Phalcon Team
