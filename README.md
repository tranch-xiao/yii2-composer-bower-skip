Yii2 Composer Bower Skip
========================

A composer package that allows you to install or update Yii2 without Bower-Asset.

[![Latest Stable Version](https://poser.pugx.org/yidas/yii2-composer-bower-skip/v/stable)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![Total Downloads](https://poser.pugx.org/yidas/yii2-composer-bower-skip/downloads)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![Latest Unstable Version](https://poser.pugx.org/yidas/yii2-composer-bower-skip/v/unstable)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)
[![License](https://poser.pugx.org/yidas/yii2-composer-bower-skip/license)](https://packagist.org/packages/yidas/yii2-composer-bower-skip)

After requiring this composer, Bower packages will not be install or update, so you need to manually update Bower-Asset if needed.

---

INSTALLATION
------------

In Yii2 `composer.json`, require `yidas/yii2-composer-bower-skip` before `yiisoft/yii2`.

Example `composer.json`:
```
"require": {
    "php": ">=5.4.0",
    "yidas/yii2-composer-bower-skip": "~2.0.0",
    "yiisoft/yii2": "~2.0.5",
    "yiisoft/yii2-bootstrap": "~2.0.0"
}
```

After that, you can run the `composer update` without handling Bower-Asset.


### How to use this for createing Yii2 project via Composer

#### Yii2-App-Basic (Fixed Bower version):

You can create Yii2 project by using [yidas/yii2-app-basic](https://github.com/yidas/yii2-app-basic) package:  

    composer create-project --prefer-dist yidas/yii2-app-basic

This package is Yii 2 Basic Application Template with fixed Bower vendor, which including `yii2-composer-bower-skip` already.


#### Official Archive File:

You can download Yii2 from official [Archive File](http://www.yiiframework.com/download/) then manally install `yii2-composer-bower-skip` on it.

---

### Install & update Bower-Asset via Composer 

Thanks to [Asset-Packagist](https://asset-packagist.org/), you may install Bower smoothly in Yii2 with [new version](https://github.com/yiisoft/yii2-app-basic/commit/fc2ec7dfee9313288171e2fe8a5b80e22c1e1509) since release on Packagist. 

Check your Yii2 application config before using asset-packagist:

```php
$config = [
    ...
    'aliases' => [
        '@bower' => '@vendor/bower-asset',
        '@npm'   => '@vendor/npm-asset',
    ],
    ...
];
```
