# Yii2-Composer-Bower-skip

A composer package that allows you to install or update yii2 without bower-asset (without composer-asset-plugin).

After requiring this composer, Bower packages will not be updated, so you may need to manually update Bower-Asset when the further update of Yii2 core is needed.

---

## How to use?

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

After that, you can do the `composer update` without bower-asset.

---

## How to use when installing Yii2 via Composer

If you did not install yii from an Archive File but installed via Composer, we don't recommend you to globally require `yii2-composer-bower-skip` before create-project.

Instead, you can install Yii2 by using [yidas/yii2-app-light](https://github.com/yidas/yii2-app-light) package:

    php composer.phar create-project yidas/yii2-app-light

Above package includes yii2 framework with `yii2-composer-bower-skip` requiring in `composer.json` file already.

---

## How to install & update bower-asset via Composer 

If you need to use bower-asset package with Composer updating, instead of using this package, you can require [Composer Asset Plugin](https://github.com/fxpio/composer-asset-plugin) before install or update Composer: 

```
composer global require "fxp/composer-asset-plugin:^1.2.0"
```
