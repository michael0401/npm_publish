##Things need to know for publishing a module to [npm](#https://npmjs.org)

###HOW TO CREATE PACKAGE.JSON?
package.json is a necessary file when you want to publish you module to [npm](#https://npmjs.org).

1. Go to the directory of that module in the shell (inside the folder of that module).
2. Type in following commands:
    
    <code>npm init</code>  
3. Follow the steps and answer all the questions (For every question, the npm will provide you with default answer, just press enter if you don't want to change it).
4. After you answer all the questions, npm will present you the information in the the package.json. You can either type "yes" to create the package.json or type "no" to abort.
5. The variables of package.json you can set in this way are very limit. You can add new variables or changing the existing variable values by directly editing the package.json file. 
For example, if you want to add <strong>dependencies</strong> and <strong>devDependencies</strong> (<strong>dependencies</strong> are the modules needed to run and develop. <strong>devDependencies</strong> are the modules ONLY needed for development purpose.) 

__Original package.json:__

        {
        "author": "xxx",
        "license": "xx",
        "readmeFilename": "README.md",
        "gitHead": "xxx"
        }
        
__We want to add underscore with version highter than 1.0.0 as both dependencies and devDependencies. After adding dependencies and devDependencies:__

        {
        "author": "xxx",
        "license": "xx",
        "readmeFilename": "README.md",
        "gitHead": "xxx",
        "dependencies": {
            "underscore": ">=1.0.0"
        },
        "devDependencies": {
           "underscore": ">=1.0.0"
        }
        }
###HOW TO PUBLISH?
By publishing you module to [npm](#https://npmjs.org), you can allow other people to install you module by using npm.

1. Make sure that you have successfully created package.json and README.md for that module.
2. Go to the directory that contains the folder of that module (outside the folder of that module).
3. Type in following commands:
 
    <code>npm publish \<folder-name\></code>
4. Go to https://npmjs.org and search to check if the module is published successfully.

###HOW TO DELETE?
After you succesfully publish your module, you can also delete it from [npm](#https://npmjs.org).

* To delete the entire module (all versions), type in commands: 

    <code>npm unpublish \<module-name\> --force</code>
* To delete a specific version, type in commands:

    <code>npm unpublish \<module-name\>@\<version\></code>
    
###HOW TO PUBLISH A NEW VERSION?
After you modify you module, you can publish a latest version to replace the old one.

1. The version should be "0.0.0" syntax. Change the version to a new one in the package.json file (Use <code>npm init</code> or edit package.json).
2. Publish the module.
