Yii2 Composer Bower Skip
========================

[![Latest Stable Version](https://poser.pugx.org/yidas/yii2-composer-bower-skip/v/stable)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![Total Downloads](https://poser.pugx.org/yidas/yii2-composer-bower-skip/downloads)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![Latest Unstable Version](https://poser.pugx.org/yidas/yii2-composer-bower-skip/v/unstable)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![License](https://poser.pugx.org/yidas/yii2-composer-bower-skip/license)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)

A composer package that allows you to install or update yii2 without Bower-Asset.

After requiring this composer, Bower packages will not be install or update, so you need to manually update Bower-Asset if needed.

---

INSTALLATION
------------

In yii2 `composer.json`, require `yidas/yii2-composer-bower-skip` before `yiisoft/yii2`.

Example json:
```
"require": {
    "php": ">=5.4.0",
    "yidas/yii2-composer-bower-skip": "~2.0.0",
    "yiisoft/yii2": "~2.0.5",
    "yiisoft/yii2-bootstrap": "~2.0.0"
}
```

After that, you can run the `composer update` without Bower-Asset.


### How to use this for createing Yii2 project via Composer

If you did not install Yii2 from an [Archive File](http://www.yiiframework.com/download/) but installed via Composer, there are some ways to create Yii2 project smoothly:

1. You can create Yii2 project by using [yidas/yii2-app-lite](https://github.com/yidas/yii2-app-lite) package:

    composer create-project yidas/yii2-app-lite

This package contains yii2 framework with `yii2-composer-bower-skip` so that you don't need to handle Bower.

2. Thanks to [Asset-Packagist](https://asset-packagist.org/), you may install Yii2 smoothly with [new version](https://github.com/yiisoft/yii2-app-basic/commit/fc2ec7dfee9313288171e2fe8a5b80e22c1e1509) since release on Packagist.


### Install & update Bower-Asset via Composer 

You can use [Asset-Packagist](https://asset-packagist.org/) to install or update Bower-Asset.

Check you Yii2 application config before using asset-packagist:

    $config = [
        ...
        'aliases' => [
            '@bower' => '@vendor/bower-asset',
            '@npm'   => '@vendor/npm-asset',
        ],
        ...
    ];
