Yii Framework 2 Change Log
==========================

2.0.0 beta under development
----------------------------

- Bug #1326: The `visible` setting for `DetailView` doesn't work as expected (qiangxue)
- Bug #1446: Logging while logs are processed causes infinite loop (qiangxue)
- Bug #1497: Localized view files are not correctly returned (mintao)
- Bug #1500: Log messages exported to files are not separated by newlines (omnilight, qiangxue)
- Bug #1504: Debug toolbar isn't loaded successfully in some environments when xdebug is enabled (qiangxue)
- Bug #1509: The SQL for creating Postgres RBAC tables is incorrect (qiangxue)
- Bug #1545: It was not possible to execute db Query twice, params where missing (cebe)
- Bug #1550: fixed the issue that JUI input widgets did not property input IDs.
- Bug #1654: Fixed the issue that a new message source object is generated for every new message being translated (qiangxue)
- Bug #1582: Error messages shown via client-side validation should not be double encoded (qiangxue)
- Bug #1591: StringValidator is accessing undefined property (qiangxue)
- Bug #1597: Added `enableAutoLogin` to basic and advanced application templates so "remember me" now works properly (samdark)
- Bug #1631: Charset is now explicitly set to UTF-8 when serving JSON (samdark)
- Bug #1635: `yii\jui\SliderInput` wasn't properly initialized (samdark)
- Bug #1686: ActiveForm is creating duplicated messages in error summary (qiangxue)
- Bug #1704: Incorrect regexp is used in `Inflector::camelize()` (qiangxue)
- Bug #1710: OpenId auth client does not request required attributes correctly (klimov-paul)
- Bug #1798: Fixed label attributes for array fields (zhuravljov)
- Bug #1800: Better check for `$_SERVER['HTTPS']` in `yii\web\Request::getIsSecureConnection()` (ginus, samdark)
- Bug #1827: Debugger toolbar is loaded twice if an action is calling `run()` to execute another action (qiangxue)
- Bug #1868: Added ability to exclude tables from FixtureController apply/clear actions. (Ragazzo)
- Bug #1869: Fixed tables clearing. `TRUNCATE` changed to `DELETE` to avoid postgresql tables checks (and truncating all tables) (Ragazzo)
- Bug #1870: Validation errors weren't properly translated when using clientside validation (samdark)
- Bug #1930: Fixed domain based URL matching for website root (samdark)
- Bug #1937: Fixed wrong behavior or advanced app's `init --env` when called without parameter actually specified (samdark)
- Bug #1959: `Html::activeCheckbox` wasn't respecting custom values for checked/unchecked state (klevron, samdark)
- Bug #1965: `Controller::findLayoutFile()` returns incorrect file path when layout name starts with a slash (qiangxue)
- Bug #1992: In module scenario that use 'site/captcha' will get wrong refreshUrl (callmez)
- Bug #1993: afterFind event in AR is now called after relations have been populated (cebe, creocoder)
- Bug #1998: Unchecked required checkbox never pass client validation (klevron)
- Bug: Fixed `Call to a member function registerAssetFiles() on a non-object` in case of wrong `sourcePath` for an asset bundle (samdark)
- Bug: Fixed incorrect event name for `yii\jui\Spinner` (samdark)
- Bug: Json::encode() did not handle objects that implement JsonSerializable interface correctly (cebe)
- Bug: Fixed issue with tabular input on ActiveField::radio() and ActiveField::checkbox() (jom)
- Bug: Fixed the issue that query cache returns the same data for the same SQL but different query methods (qiangxue)
- Bug: Fixed URL parsing so it's now properly giving 404 for URLs like `http://example.com//////site/about` (samdark)
- Bug: Fixed `HelpController::getModuleCommands` issue where it attempts to scan a module's controller directory when it doesn't exist (jom)
- Enh #46: Added Image extension based on [Imagine library](http://imagine.readthedocs.org) (tonydspaniard)
- Enh #364: Improve Inflector::slug with `intl` transliteration. Improved transliteration char map. (tonydspaniard)
- Enh #797: Added support for validating multiple columns by `UniqueValidator` and `ExistValidator` (qiangxue)
- Enh #802: Added support for retrieving sub-array element or child object property through `ArrayHelper::getValue()` (qiangxue, cebe)
- Enh #1293: Replaced Console::showProgress() with a better approach. See Console::startProgress() for details (cebe)
- Enh #1406: DB Schema support for Oracle Database (p0larbeer, qiangxue)
- Enh #1437: Added ListView::viewParams (qiangxue)
- Enh #1469: ActiveRecord::find() now works with default conditions (default scope) applied by createQuery (cebe)
- Enh #1476: Add yii\web\Session::handler property (nineinchnick)
- Enh #1499: Added `ActionColumn::controller` property to support customizing the controller for handling GridView actions (qiangxue)
- Enh #1523: Query conditions now allow to use the NOT operator (cebe)
- Enh #1552: It is now possible to use multiple bootstrap NavBar in a single page (Alex-Code)
- Enh #1572: Added `yii\web\Controller::createAbsoluteUrl()` (samdark)
- Enh #1579: throw exception when the given AR relation name does not match in a case sensitive manner (qiangxue)
- Enh #1581: Added `ActiveQuery::joinWith()` and `ActiveQuery::innerJoinWith()` to support joining with relations (qiangxue)
- Enh #1601: Added support for tagName and encodeLabel parameters in ButtonDropdown (omnilight)
- Enh #1611: Added `BaseActiveRecord::markAttributeDirty()` (qiangxue)
- Enh #1633: Advanced application template now works with MongoDB by default (samdark)
- Enh #1634: Use masked CSRF tokens to prevent BREACH exploits (qiangxue)
- Enh #1641: Added `BaseActiveRecord::updateAttributes()` (qiangxue)
- Enh #1646: Added postgresql `QueryBuilder::checkIntegrity` and `QueryBuilder::resetSequence` (Ragazzo)
- Enh #1645: Added `Connection::$pdoClass` property (Ragazzo)
- Enh #1681: Added support for automatically adjusting the "for" attribute of label generated by `ActiveField::label()` (qiangxue)
- Enh #1706: Added support for registering a single JS/CSS file with dependency (qiangxue)
- Enh #1773: keyPrefix property of Cache is not restricted to alnum characters anymore, however it is still recommended (cebe)
- Enh #1809: Added support for building "EXISTS" and "NOT EXISTS" query conditions (abdrasulov)
- Enh #1852: ActiveRecord::tableName() now returns table name using DbConnection::tablePrefix (creocoder)
- Enh #1894: The path aliases `@webroot` and `@web` are now available right after the application is initialized (qiangxue)
- Enh #1921: Grid view ActionColumn now allow to name buttons like `{controller/action}` (creocoder)
- Enh #1973: `yii message/extract` is now able to generate `.po` files (SergeiKutanov, samdark)
- Enh #1984: ActionFilter will now mark event as handled when action run is aborted (cebe)
- Enh #2003: Added `filter` property to `ExistValidator` and `UniqueValidator` to support adding additional filtering conditions (qiangxue)
- Enh #2043: Added support for custom request body parsers (danschmidt5189, cebe)
- Enh #2051: Do not save null data into database when using RBAC (qiangxue)
- Enh: Added `favicon.ico` and `robots.txt` to default application templates (samdark)
- Enh: Added `Widget::autoIdPrefix` to support prefixing automatically generated widget IDs (qiangxue)
- Enh: Support for file aliases in console command 'message' (omnilight)
- Enh: Sort and Pagination can now create absolute URLs (cebe)
- Enh: Added support for using array-typed arguments for console commands (qiangxue)
- Enh: Added support for installing packages conforming to PSR-4 standard (qiangxue)
- Enh: Better exception message when class cannot be loaded (samdark)
- Enh: `init` of advanced application now allows to specify answer for overwriting files via `init --overwrite=n` (samdark)
- Enh: Added `TableSchema::fullName` property (qiangxue)
- Enh #1839: Added support for getting file extension and basename from uploaded file (anfrantic)
- Enh: yii\codeception\TestCase now supports loading and using fixtures via Yii fixture framework (qiangxue)
- Enh: Added support to parse json request data to Request::getRestParams() (cebe)
- Chg #1519: `yii\web\User::loginRequired()` now returns the `Response` object instead of exiting the application (qiangxue)
- Chg #1586: `QueryBuilder::buildLikeCondition()` will now escape special characters and use percentage characters by default (qiangxue)
- Chg #1610: `Html::activeCheckboxList()` and `Html::activeRadioList()` will submit an empty string if no checkbox/radio is selected (qiangxue)
- Chg #1643: Added default value for `Captcha::options` (qiangxue)
- Chg #1796: Removed `yii\base\Controller::getActionParams()` (samdark)
- Chg #1835: `CheckboxColumn` now renders checkboxes whose values are the corresponding data key values (qiangxue)
- Chg #1821: Changed default values for yii\db\Connection username and password to null (cebe)
- Chg #1844: `Response::sendFile()` and other file sending methods will not send the response (qiangxue)
- Chg #1852: DbConnection::tablePrefix default value now 'tbl_' (creocoder)
- Chg #2057: AutoTimestamp attributes defaults changed from `create_time` and `update_time` to `created_at` and `updated_at` (creocoder)
- Chg #2063: Removed `yii\web\Request::acceptTypes` and renamed `yii\web\Request::acceptedContentTypes` to `acceptableContentTypes` (qiangxue)
- Chg: Renamed `yii\jui\Widget::clientEventsMap` to `clientEventMap` (qiangxue)
- Chg: Renamed `ActiveRecord::getPopulatedRelations()` to `getRelatedRecords()` (qiangxue)
- Chg: Renamed `attributeName` and `className` to `targetAttribute` and `targetClass` for `UniqueValidator` and `ExistValidator` (qiangxue)
- Chg: Added `yii\widgets\InputWidget::options` (qiangxue)
- Chg: Changed the signature of `urlCreator` and button creators for `yii\gridview\ActionColumn` (qiangxue)
- Chg: Updated HTMLPurified dependency to `4.6.*`.
- Chg: Changed Yii autoloader to support loading PSR-4 classes only (i.e. PEAR-styled classes not supported anymore) (qiangxue)
- Chg: Changed the directory structure according to PSR-4. You have to update your application `index.php`,
       `index-test.php` and `yii` files to point to the new location of `Yii.php` (qiangxue, cebe)
- Chg: Advanced app template: moved database connection DSN, login and password to `-local` config not to expose it to VCS (samdark)
- Chg: Renamed `yii\web\Request::acceptedLanguages` to `acceptableLanguages` (qiangxue)
- New #66: [Auth client library](https://github.com/yiisoft/yii2-authclient) OpenId, OAuth1, OAuth2 clients (klimov-paul)
- New #1393: [Codeception testing framework integration](https://github.com/yiisoft/yii2-codeception) (Ragazzo)
- New #1438: [MongoDB integration](https://github.com/yiisoft/yii2-mongodb) ActiveRecord and Query (klimov-paul)
- New #1956: Implemented test fixture framework (qiangxue)
- New: Yii framework now comes with core messages in multiple languages
- New: Added yii\codeception\DbTestCase (qiangxue)


2.0.0 alpha, December 1, 2013
---------------------------

- Initial release.
- Official extensions released in this version:
  - [Twitter bootstrap 3.0](https://github.com/yiisoft/yii2-bootstrap)
  - [Jquery UI](https://github.com/yiisoft/yii2-jui)

  - [Debug Toolbar](https://github.com/yiisoft/yii2-debug)
  - [Gii code generator](https://github.com/yiisoft/yii2-gii)

  - [Elasticsearch integration](https://github.com/yiisoft/yii2-elasticsearch): ActiveRecord and Query
  - [Redis integration](https://github.com/yiisoft/yii2-redis): ActiveRecord, Cache and Session
  - [Sphinx integration](https://github.com/yiisoft/yii2-sphinx): ActiveRecord and Query

  - [Swiftmailer](https://github.com/yiisoft/yii2-swiftmailer)

  - [Smarty View Renderer](https://github.com/yiisoft/yii2-smarty)
  - [Twig View Renderer](https://github.com/yiisoft/yii2-twig)