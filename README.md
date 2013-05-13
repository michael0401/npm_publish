##Things need to know for publishing a module to [npm](#https://npmjs.org)

###HOW TO CREATE PACKAGE.JSON?
package.json is a necessary file when you want to publish you module to [npm](#https://npmjs.org).

1. Go to the directory of that module in the shell (inside the folder of that module).
2. Type in following commands:
    
    <code>npm init</code>  
3. Follow the steps and answer all the questions(For every question, the npm will provide you with default answer, just press enter if you don't want to change it).
4. After you answer all the questions, npm will present you the information in the the package.json. You can either type "yes" to create the package.json or type "no" to abort.

###HOW TO PUBLISH?
By publishing you module to [npm](#https://npmjs.org), you can allow other people to install you module by using npm.

1. Make sure that you have successfully created package.json and README.md for that module.
2. Go to the directory that contains the folder of that module (outside the folder of that module).
3. Type in following commands:
 
    <code>npm publish \<folder-name\></code>
4. Go to https://npmjs.org and search to check if the module is published successfully.

###HOW TO DELETE?
After you succesfully publish your module, you can also delete it from [npm](#https://npmjs.org).

* To delete the entire module( all versions), type in commands: 

    <code>npm unpublish \<module-name\> --force</code>
* To delete a specific version, type in commands:

    <code>npm unpublish \<module-name\>@\<version\></code>
    
###HOW TO PUBLISH A NEW VERSION?
After you modify you module, you can publish a latest version to replace the old one.

1. The version standard should start from "0.0.0" and always in this format. Change the version to a new one in the package.json file (Use <code>npm init</code>).
2. Publish the module.
