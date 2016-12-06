# yii2-composer-bower-skip

A composer package that allows you to install yii2 without bower-asset (without composer-asset-plugin).

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
