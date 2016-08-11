# phonegap-cordova-dependence
Given a PhoneGap project, pin Cordova as a dependency.

Using npm, the latest Cordova release will be pinned with 'npm install cordova --save' if no dependency is declared in the package.json of the project. 

# Usage
## Parameters
 * @param  {Path[String]} projectDir [Path to anywhere within the PhoneGap project being modified]
 * @optional_param  {EventEmitter|False} extEvents   [Used for events emitting. If undefined, 'log' and 'warn' will log to console. If false, will silence logging]
 * @return {Promise|Error}            [Returns the project root path or a cordova error.]

## Example
```
var cordovaDependency = require('phonegap-cordova-dependence');

cordovaDependency.exec(path_to_project)
  .fail(function (err) {
    console.log('\033[1m \033[31m Error adding Cordova dependency to project: ' + err.message);
    throw err;
});
```
