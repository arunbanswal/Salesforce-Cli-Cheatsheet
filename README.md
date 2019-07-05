# Salesforce cli Cheatsheet

## Table of contents
* [`force:alias:list`](#force-alias-list)
* [`force:alias:set`](#force-alias-set)
* [`force:apex:class:create`](#force-apex-class-create)
* [`force:apex:execute`](#force-apex-execute)
* [`force:apex:log:get`](#force-apex-log-get)
* [`force:apex:log:list`](#force-apex-log-list)
* [`force:apex:log:tail`](#force-apex-log-tail)
* [`force:apex:test:report`](#force-apex-test-report)
* [`force:apex:test:run`](#force-apex-test-run)
* [`force:apex:trigger:create`](#force-apex-trigger-create)
* [`force:auth:jwt:grant`](#force-auth-jwt-grant)
* [`force:auth:list`](#force-auth-list)
* [`force:auth:logout`](#force-auth-logout)
* [`force:auth:sfdxurl:store`](#force-auth-sfdxurl-store)
* [`force:auth:web:login`](#force-auth-web-login)
* [`force:config:get`](#force-config-get)
* [`force:config:list`](#force-config-list)
* [`force:config:set`](#force-config-set)
* [`force:data:bulk:delete`](#force-data-bulk-delete)
* [`force:data:bulk:status`](#force-data-bulk-status)
* [`force:data:bulk:upsert`](#force-data-bulk-upsert)
* [`force:data:record:create`](#force-data-record-create)
* [`force:data:record:delete`](#force-data-record-delete)
* [`force:data:record:get`](#force-data-record-get)
* [`force:data:record:update`](#force-data-record-update)
* [`force:data:soql:query`](#force-data-soql-query)
* [`force:data:tree:export`](#force-data-tree-export)
* [`force:data:tree:import`](#force-data-tree-import)
* [`force:doc:commands:display`](#force-doc-commands-display)
* [`force:doc:commands:list`](#force-doc-commands-list)
* [`force:lightning:app:create`](#force-lightning-app-create)
* [`force:lightning:component:create`](#force-lightning-component-create)
* [`force:lightning:event:create`](#force-lightning-event-create)
* [`force:lightning:interface:create`](#force-lightning-interface-create)
* [`force:lightning:lint`](#force-lightning-lint)
* [`force:lightning:test:create`](#force-lightning-test-create)
* [`force:lightning:test:install`](#force-lightning-test-install)
* [`force:lightning:test:run`](#force-lightning-test-run)
* [`force:limits:api:display`](#force-limits-api-display)
* [`force:mdapi:convert`](#force-mdapi-convert)
* [`force:mdapi:deploy`](#force-mdapi-deploy)
* [`force:mdapi:deploy:cancel`](#force-mdapi-deploy-cancel)
* [`force:mdapi:deploy:report`](#force-mdapi-deploy-report)
* [`force:mdapi:describemetadata`](#force-mdapi-describemetadata)
* [`force:mdapi:listmetadata`](#force-mdapi-listmetadata)
* [`force:mdapi:retrieve`](#force-mdapi-retrieve)
* [`force:mdapi:retrieve:report`](#force-mdapi-retrieve-report)
* [`force:org:clone`](#force-org-clone)
* [`force:org:create`](#force-org-create)
* [`force:org:delete`](#force-org-delete)
* [`force:org:display`](#force-org-display)
* [`force:org:list`](#force-org-list)
* [`force:org:open`](#force-org-open)
* [`force:org:shape:create`](#force-org-shape-create)
* [`force:org:shape:delete`](#force-org-shape-delete)
* [`force:org:shape:list`](#force-org-shape-list)
* [`force:org:snapshot:create`](#force-org-snapshot-create)
* [`force:org:snapshot:delete`](#force-org-snapshot-delete)
* [`force:org:snapshot:get`](#force-org-snapshot-get)
* [`force:org:snapshot:list`](#force-org-snapshot-list)
* [`force:org:status`](#force-org-status)
* [`force:package1:version:create`](#force-package1-version-create)
* [`force:package1:version:create:get`](#force-package1-version-create-get)
* [`force:package1:version:display`](#force-package1-version-display)
* [`force:package1:version:list`](#force-package1-version-list)
* [`force:package:create`](#force-package-create)
* [`force:package:hammertest:list`](#force-package-hammertest-list)
* [`force:package:hammertest:report`](#force-package-hammertest-report)
* [`force:package:hammertest:run`](#force-package-hammertest-run)
* [`force:package:install`](#force-package-install)
* [`force:package:install:report`](#force-package-install-report)
* [`force:package:installed:list`](#force-package-installed-list)
* [`force:package:list`](#force-package-list)
* [`force:package:uninstall`](#force-package-uninstall)
* [`force:package:uninstall:report`](#force-package-uninstall-report)
* [`force:package:update`](#force-package-update)
* [`force:package:version:create`](#force-package-version-create)
* [`force:package:version:create:list`](#force-package-version-create-list)
* [`force:package:version:create:report`](#force-package-version-create-report)
* [`force:package:version:list`](#force-package-version-list)
* [`force:package:version:promote`](#force-package-version-promote)
* [`force:package:version:report`](#force-package-version-report)
* [`force:package:version:update`](#force-package-version-update)
* [`force:project:create`](#force-project-create)
* [`force:project:upgrade`](#force-project-upgrade)
* [`force:schema:sobject:describe`](#force-schema-sobject-describe)
* [`force:schema:sobject:list`](#force-schema-sobject-list)
* [`force:source:convert`](#force-source-convert)
* [`force:source:delete`](#force-source-delete)
* [`force:source:deploy`](#force-source-deploy)
* [`force:source:deploy:cancel`](#force-source-deploy-cancel)
* [`force:source:deploy:report`](#force-source-deploy-report)
* [`force:source:open`](#force-source-open)
* [`force:source:pull`](#force-source-pull)
* [`force:source:push`](#force-source-push)
* [`force:source:retrieve`](#force-source-retrieve)
* [`force:source:status`](#force-source-status)
* [`force:user:create`](#force-user-create)
* [`force:user:display`](#force-user-display)
* [`force:user:list`](#force-user-list)
* [`force:user:password:generate`](#force-user-password-generate)
* [`force:user:permset:assign`](#force-user-permset-assign)
* [`force:visualforce:component:create`](#force-visualforce-component-create)
* [`force:visualforce:page:create`](#force-visualforce-page-create)
* [`plugins`](#plugins)
* [`plugins:generate`](#plugins-generate)
* [`plugins:install`](#plugins-install)
* [`plugins:link`](#plugins-link)
* [`plugins:trust:sign`](#plugins-trust-sign)
* [`plugins:trust:verify`](#plugins-trust-verify)
* [`plugins:uninstall`](#plugins-uninstall)
* [`plugins:update`](#plugins-update)
* [`update`](#update)
* [`which`](#which)
* [`help`](#help)


## force

###### USAGE

```
sfdx force
```
<a id="force-alias-list" />

### `force:alias:list`

###### USAGE

```
sfdx force:alias:list
```

###### DESCRIPTION

Example:

```
sfdx force:alias:list
```

<a id="force-alias-set" />

### `force:alias:set`

###### USAGE
```
sfdx force:alias:set name=value...
```

###### DESCRIPTION
  You can associate an alias with only one username at a time. If you’ve set an alias multiple times, the alias points to the most recent username.
  To delete an alias, run "```sfdx force:alias:set```" with no username.

  Examples:
  
```
sfdx force:alias:set YourAlias=username@example.com      
sfdx force:alias:set YourAlias=username@example.com YourOtherAlias=devhub@example.com
sfdx force:alias:set AliasToDelete=
```
	  
<a id="force-apex-class-create" />

### `force:apex:class:create`

###### USAGE
```
sfdx force:apex:class:create -n <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --classname=classname\
      (required) name of the generated Apex class

  + -t, --template=DefaultApexClass|ApexException|ApexUnitTest|InboundEmailService\
      [default: DefaultApexClass] template to use for file creation


###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.

  Examples:
```
sfdx force:apex:class:create -n MyClass
sfdx force:apex:class:create -n MyClass -d classes
```
	  
<a id="force-apex-execute" />

### `force:apex:execute`

###### USAGE
```
sfdx force:apex:execute [-f <filepath>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --apexcodefile=apexcodefile\
      path to a local file containing Apex code

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Executes one or more lines of Apex code, or executes the code in a local file.
  Before you enter code, run this command with no parameters to get a prompt.
  From the prompt, all commands are executed in a single execute anonymous request.
  For more information, see "Anonymous Blocks" in the Apex Developer Guide.

  Examples:
```
sfdx force:apex:execute -f ~/test.apex
sfdx force:apex:execute
```

```
>> Start typing Apex code. Press the Enter key after each line,
>> then press CTRL+D when finished.
```
	  
<a id="force-apex-log-get" />

### `force:apex:log:get`

###### USAGE

```
sfdx force:apex:log:get [-c] [-i <id> | -n <number>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -c, --color\
      colorize noteworthy log lines

  + -i, --logid=logid\
      ID of the log to display

  + -n, --number=number\
      number of most recent logs to display

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command


###### DESCRIPTION
  When you execute this command in a project, it fetches the specified log or given number of last logs from your default scratch org.
  To get the IDs for your debug logs, run "```sfdx force:apex:log:list```".
  To specify a count of logs to return, use the --number parameter to return the most recent logs.
  Executing this command without parameters returns the most recent log.

  Examples:
  
```
sfdx force:apex:log:get -i <log id>
sfdx force:apex:log:get -i <log id> -u me@my.org
sfdx force:apex:log:get -n 2 -c
```

<a id="force-apex-log-list" />

### `force:apex:log:list`

###### USAGE
  sfdx force:apex:log:list [-u <string>] [--apiversion <string>]

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
  

###### DESCRIPTION
  When you execute this command in a project, it lists the log IDs for your default scratch org.

  Examples:
  
```
sfdx force:apex:log:list
sfdx force:apex:log:list -u me@my.org
```
	  
<a id="force-apex-log-tail" />

### `force:apex:log:tail`

###### USAGE

```
sfdx force:apex:log:tail [-c] [-d <string>] [-s] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -c, --color\
      colorize noteworthy log lines

  + -d, --debuglevel=debuglevel\
      debug level for trace flag

  + -s, --skiptraceflag\
      skip trace flag setup

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
  

###### DESCRIPTION
  Tails logs from your target org for 30 minutes.
  If a DEVELOPER_LOG trace flag does not exist, this command creates one in the target org.
  If the active trace flag's expiration date is within this command's timeout window, the command sets the trace flag's expiration date to 30 minutes from the current time.
  The --debuglevel parameter assigns a debug level to the active DEVELOPER_LOG trace flag.
  Use --skiptraceflag to skip trace flag setup, including setting expiration date and debug level. Include this flag only if there is an active user-based trace flag for your user.
  The --json parameter emits log lines in JSON, but does not follow the standard Salesforce CLI JSON format (which includes status and result values).

  Examples:
```
sfdx force:apex:log:tail
sfdx force:apex:log:tail --debuglevel MyDebugLevel
sfdx force:apex:log:tail -c -s
```
	  
<a id="force-apex-test-report" />

### `force:apex:test:report`

###### USAGE
```
sfdx force:apex:test:report -i <id> [-c] [-d <directory>] [-w <minutes>] [-r human|tap|junit|json] [-u <string>] [--apiversion <string>] [--verbose]
```
 

###### OPTIONS
  + -c, --codecoverage\
      retrieve code coverage results

  + -d, --outputdir=outputdir\
      directory to store test run files

  + -i, --testrunid=testrunid\
      (required) ID of test run

  + -r, --resultformat=(human|tap|junit|json)\
      [default: human] result format emitted to stdout; --json flag overrides this parameter

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] the streaming client socket timeout (in minutes)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
	  
  + --verbose\
      display Apex test processing details

###### DESCRIPTION
  Displays test results for an enqueued or completed asynchronous Apex test run.

  Examples:
  
```
sfdx force:apex:test:report -i <test run id>
sfdx force:apex:test:report -i <test run id> -r junit
sfdx force:apex:test:report -i <test run id> -c --json
```
	  
<a id="force-apex-test-run" />

### `force:apex:test:run`

###### USAGE
```
sfdx force:apex:test:run [-n <array> | -s <array> | -t <array>] [-c] [-d <directory>] [-l RunLocalTests|RunAllTestsInOrg|RunSpecifiedTests] [-w <minutes>] [-y] [-r human|tap|junit|json] [-u <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -c, --codecoverage\
      retrieve code coverage results

  + -d, --outputdir=outputdir\
      directory to store test run files

  + -l, --testlevel=(RunLocalTests|RunAllTestsInOrg|RunSpecifiedTests)\
      testlevel enum value

  + -n, --classnames=classnames\
      comma-separated list of Apex test class names to run

  + -r, --resultformat=(human|tap|junit|json)\
      result format emitted to stdout; --json flag overrides this parameter

  + -s, --suitenames=suitenames\
      comma-separated list of Apex test suite names to run

  + -t, --tests=tests\
      comma-separated list of Apex test class names or IDs and, if applicable, test methods to run

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      the streaming client socket timeout (in minutes)

  + -y, --synchronous\
      run tests from a single class synchronously

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      display Apex test processing details

###### DESCRIPTION
  By default, runs all Apex tests in the org’s namespace.
  To run specific test classes, specify class names or suite names, or set a --testlevel value.
  To run specific test methods, use --tests.

  Examples:
  
```  
sfdx force:apex:test:run
sfdx force:apex:test:run -n MyClassTest,MyOtherClassTest -r human
sfdx force:apex:test:run -s MySuite,MyOtherSuite -c --json
sfdx force:apex:test:run -t MyClassTest.testCoolFeature,MyClassTest.testAwesomeFeature,AnotherClassTest,namespace.TheirClassTest.testThis -r human
sfdx force:apex:test:run -l RunLocalTests -d <path to outputdir> -u me@my.org
```

<a id="force-apex-trigger-create" />

### `force:apex:trigger:create`

###### USAGE

```
sfdx force:apex:trigger:create -n <string> [-t <string>] [-d <string>] [-s <string>] [-e <array>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -e, --triggerevents=triggerevents\
      [default: before insert] events that fire the trigger (before insert|before update|before delete|after insert|after update|after delete|after undelete)

  + -n, --triggername=triggername\
      (required) name of the generated Apex trigger

  + -s, --sobject=sobject\
      [default: SOBJECT] sObject to create a trigger on

  + -t, --template=ApexTrigger\
      [default: ApexTrigger] template to use for file creation



###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.

  Examples:
```
sfdx force:apex:trigger:create -n MyTrigger
sfdx force:apex:trigger:create -n MyTrigger -s Account -e 'before insert, after upsert'
sfdx force:apex:trigger:create -n MyTrigger -d triggers
```

<a id="force-auth-jwt-grant" />

### `force:auth:jwt:grant`

###### USAGE
```
sfdx force:auth:jwt:grant -u <string> -f <filepath> -i <string> [-r <url>] [-d] [-s] [-a <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      set an alias for the authenticated org

  + -d, --setdefaultdevhubusername\
      set the authenticated org as the default dev hub org for scratch org
      creation

  + -f, --jwtkeyfile=jwtkeyfile\
      (required) path to a file containing the private key

  + -i, --clientid=clientid\
      (required) OAuth client ID (sometimes called the consumer key)

  + -r, --instanceurl=instanceurl\
      the login URL of the instance the org lives on

  + -s, --setdefaultusername\
      set the authenticated org as the default username that all commands run
      against

  + -u, --username=username\
      (required) authentication username

###### DESCRIPTION
  Authorizes a Salesforce org using a private key file that has been uploaded to a personal connected app.

  If you specify an --instanceurl value, this value overrides the sfdcLoginUrl value in your sfdx-project.json file. To specify a My Domain URL, use the format <yourdomain>.my.salesforce.com (not <yourdomain>.lightning.force.com).

  Examples:
  
```
sfdx force:auth:jwt:grant -u me@my.org -f <path to jwt key file> -i <OAuth client id>
sfdx force:auth:jwt:grant -u me@my.org -f <path to jwt key file> -i <OAuth client id> -s -a MyDefaultOrg
sfdx force:auth:jwt:grant -u me@acme.org -f <path to jwt key file> -i <OAuth client id> -r https://acme.my.salesforce.com
```

<a id="force-auth-list" />

### `force:auth:list`

###### USAGE
```
sfdx force:auth:list
```

 
<a id="force-auth-logout" />

### `force:auth:logout`

###### USAGE
```
sfdx force:auth:logout [-a] [-p] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --all\
      include all authenticated orgs

  + -p, --noprompt\
      do not prompt for confirmation

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
  

###### DESCRIPTION

  By default, this command logs you out from your default scratch org.
  
  Examples:
```
sfdx force:auth:logout -u me@my.org
sfdx force:auth:logout -a
sfdx force:auth:logout -p
```

<a id="force-auth-sfdxurl-store" />

### `force:auth:sfdxurl:store`

###### USAGE
```
sfdx force:auth:sfdxurl:store -f <filepath> [-d] [-s] [-a <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      set an alias for the authenticated org

  + -d, --setdefaultdevhubusername\
      set the authenticated org as the default dev hub org for scratch org
      creation

  + -f, --sfdxurlfile=sfdxurlfile\
      (required) path to a file containing the sfdx url

  + -s, --setdefaultusername\
      set the authenticated org as the default username that all commands run against

###### DESCRIPTION
  Authorize a Salesforce org using an SFDX auth URL stored within a file.
  The file must have the format "force://<refreshToken>@<instanceUrl>" or "force://<clientId>:<clientSecret>:<refreshToken>@<instanceUrl>".
  The file must contain only the URL or be a JSON file that has a top-level property named sfdxAuthUrl.

  Examples:

```
sfdx force:auth:sfdxurl:store -f <path to sfdxAuthUrl file>
sfdx force:auth:sfdxurl:store -f <path to sfdxAuthUrl file> -s -a MyDefaultOrg
```

<a id="force-auth-web-login" />

### `force:auth:web:login`

###### USAGE
```
sfdx force:auth:web:login [-i <string>] [-r <url>] [-d] [-s] [-a <string>] 
```

###### OPTIONS
  + -a, --setalias=setalias\
      set an alias for the authenticated org

  + -d, --setdefaultdevhubusername\
      set the authenticated org as the default dev hub org for scratch org creation

  + -i, --clientid=clientid\
      OAuth client ID (sometimes called the consumer key)

  + -r, --instanceurl=instanceurl\
      the login URL of the instance the org lives on

  + -s, --setdefaultusername\
      set the authenticated org as the default username that all commands run against

###### DESCRIPTION
  To log in to a sandbox, set --instanceurl to https://test.salesforce.com.

  Examples:
  
```
sfdx force:auth:web:login -a TestOrg1
sfdx force:auth:web:login -i <OAuth client id>
sfdx force:auth:web:login -r https://test.salesforce.com
```

<a id="force-config-get" />

### `force:config:get`

###### USAGE
```
sfdx force:config:get [--verbose]
```

###### OPTIONS
  + --verbose\
      emit additional command output to stdout

###### DESCRIPTION
  To see your default scratch org username, include "defaultusername".
  To see your default Dev Hub, include "defaultdevhubusername".
  To see your default instance URL, include "instanceUrl".
  To see the locations where your values are set, include the --verbose flag.

  Examples:

```
sfdx force:config:get defaultusername
sfdx force:config:get defaultusername defaultdevhubusername instanceUrl
sfdx force:config:get defaultusername defaultdevhubusername --verbose
```

<a id="force-config-list" />

### `force:config:list`

###### USAGE
```
sfdx force:config:list
```

###### DESCRIPTION
  Lists the config variables that the Salesforce CLI uses for various commands and tasks.

<a id="force-config-set" />

### `force:config:set`

###### USAGE
```
sfdx force:config:set name=value... [-g]
```

###### OPTIONS
  + -g, --global\
      set config var globally (to be used from any directory)

###### DESCRIPTION
  Sets the configuration variables that the Salesforce CLI uses for various commands and tasks. Local variables apply only to your current project. Global variables apply in any directory.

  Examples:
```
sfdx force:config:set defaultusername=me@my.org defaultdevhubusername=me@myhub.org
sfdx force:config:set defaultdevhubusername=me@myhub.org -g
```

<a id="force-data-bulk-delete" />

### `force:data:bulk:delete`

###### USAGE
```
sfdx force:data:bulk:delete -s <string> -f <filepath> [-w <minutes>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --csvfile=csvfile\
      (required) the path to the CSV file containing the ids of the records to delete

  + -s, --sobjecttype=sobjecttype\
      (required) the sObject type of the records you’re deleting

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      the number of minutes to wait for the command to complete before displaying the results

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  The file must be a CSV file with only one column: "Id".
  One job can contain many batches, depending on the length of the CSV file.
  Returns a job ID and a batch ID. Use these IDs to check job status with data:bulk:status.

  Examples:

```
sfdx force:data:bulk:delete -s Account -f ./path/to/file.csv
sfdx force:data:bulk:delete -s MyObject__c -f ./path/to/file.csv
```

<a id="force-data-bulk-status" />

### `force:data:bulk:status`

###### USAGE
```
sfdx force:data:bulk:status -i <id> [-b <id>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -b, --batchid=batchid\
      the ID of the batch whose status you want to view

  + -i, --jobid=jobid\
      (required) the ID of the job you want to view or of the job whose batch you want to view

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command  

###### DESCRIPTION
  Examples:

```
sfdx force:data:bulk:status -i 750xx000000005sAAA
sfdx force:data:bulk:status -i 750xx000000005sAAA -b 751xx000000005nAAA
```

<a id="force-data-bulk-upsert" />

### `force:data:bulk:upsert`

###### USAGE
```
sfdx force:data:bulk:upsert -s <string> -f <filepath> -i <string> [-w <minutes>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --csvfile=csvfile\
      (required) the path to the CSV file that defines the records to upsert

  + -i, --externalid=externalid\
      (required) the column name of the external ID

  + -s, --sobjecttype=sobjecttype\
      (required) the sObject type of the records you want to upsert

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      the number of minutes to wait for the command to complete before displaying the results

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  

  

###### DESCRIPTION
  Inserts or updates records from a CSV file.
  One job can contain many batches, depending on the length of the CSV file.
  Returns a job ID and a batch ID. Use these IDs to check job status with data:bulk:status.

  For information about formatting your CSV file, see "Prepare CSV Files" in the Bulk API Developer Guide.

  Examples:
```
sfdx force:data:bulk:upsert -s MyObject__c -f ./path/to/file.csv -i MyField__c
sfdx force:data:bulk:upsert -s MyObject__c -f ./path/to/file.csv -i Id -w 2
```

<a id="force-data-record-create" />

### `force:data:record:create`

###### USAGE
```
sfdx force:data:record:create -s <string> -v <string> [-t] [--perflog] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -s, --sobjecttype=sobjecttype\
      (required) the type of the record you’re creating

  + -t, --usetoolingapi\
      create the record with tooling api

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --values=values\
      (required) the <fieldName>=<value> pairs you’re creating

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --perflog\
      get API performance data

###### DESCRIPTION
  The format of a field-value pair is <fieldName>=<value>.
  Enclose all field-value pairs in one set of double quotation marks, delimited by spaces.
  Enclose values that contain spaces in single quotes.

  To get data on API performance metrics, specify both --perflog and --json.

  Examples:
  
```
sfdx force:data:record:create -s Account -v "Name=Acme"
sfdx force:data:record:create -s Account -v "Name='Universal Containers'"
sfdx force:data:record:create -s Account -v "Name='Universal Containers' Website=www.example.com"
sfdx force:data:record:create -t -s TraceFlag -v "DebugLevelId=7dl170000008U36AAE StartDate=2017-12-01T00:26:04.000+0000 ExpirationDate=2017-12-01T00:56:04.000+0000 LogType=CLASS_TRACING TracedEntityId=01p17000000R6bLAAS"
sfdx force:data:record:create -s Account -v "Name=Acme" --perflog --json
```

<a id="force-data-record-delete" />

### `force:data:record:delete`

###### USAGE

```
sfdx force:data:record:delete -s <string> [-i <id>] [-w <string>] [-t] [--perflog] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --sobjectid=sobjectid\
      the ID of the record you’re deleting

  + -s, --sobjecttype=sobjecttype\
      (required) the type of the record you’re deleting

  + -t, --usetoolingapi\
      delete the record with Tooling API

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --where=where\
      a list of <fieldName>=<value> pairs to search for

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
	  
  + --perflog\
      get API performance data

###### DESCRIPTION
  Specify an sObject type and either an ID or a list of <fieldName>=<value> pairs.
  The format of a field-value pair is <fieldName>=<value>.
  Enclose all field-value pairs in one set of double quotation marks, delimited by spaces.
  Enclose values that contain spaces in single quotes.

  To get data on API performance metrics, specify both --perflog and --json.

  Examples:
  
```
sfdx force:data:record:delete -s Account -i 001D000000Kv3dl
sfdx force:data:record:delete -s Account -w "Name=Acme"
sfdx force:data:record:delete -s Account -w "Name='Universal Containers'"
sfdx force:data:record:delete -s Account -w "Name='Universal Containers' Phone='(123) 456-7890'"
sfdx force:data:record:delete -t -s TraceFlag -i 7tf170000009cU6AAI --perflog --json
```

<a id="force-data-record-get" />

### `force:data:record:get`

###### USAGE

```
sfdx force:data:record:get -s <string> [-i <id>] [-w <string>] [-t] [--perflog] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --sobjectid=sobjectid\
      the ID of the record you’re retrieving

  + -s, --sobjecttype=sobjecttype\
      (required) the type of the record you’re retrieving

  + -t, --usetoolingapi\
      retrieve the record with Tooling API

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --where=where\
      a list of <fieldName>=<value> pairs to search for

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
	  
  + --perflog\
      get API performance data

###### DESCRIPTION
  Specify an sObject type and either an ID or a list of <fieldName>=<value> pairs.
  The format of a field-value pair is <fieldName>=<value>.
  Enclose all field-value pairs in one set of double quotation marks, delimited by spaces.
  Enclose values that contain spaces in single quotes.

  To get data on API performance metrics, specify both --perflog and --json.

  Examples:
  
```
sfdx force:data:record:get -s Account -i 001D000000Kv3dl
sfdx force:data:record:get -s Account -w "Name=Acme"
sfdx force:data:record:get -s Account -w "Name='Universal Containers'"
sfdx force:data:record:get -s Account -w "Name='Universal Containers' Phone='(123) 456-7890'"
sfdx force:data:record:get -t -s TraceFlag -i 7tf170000009cUBAAY --perflog --json
```

<a id="force-data-record-update" />

### `force:data:record:update`

###### USAGE

```
sfdx force:data:record:update -s <string> -v <string> [-i <id>] [-w <string>] [-t] [--perflog] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --sobjectid=sobjectid\
      the ID of the record you’re updating

  + -s, --sobjecttype=sobjecttype\
      (required) the type of the record you’re updating

  + -t, --usetoolingapi\
      update the record with Tooling API

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --values=values\
      (required) the <fieldName>=<value> pairs you’re updating

  + -w, --where=where\
      a list of <fieldName>=<value> pairs to search for

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --perflog\
      get API performance data

###### DESCRIPTION
  The format of a field-value pair is <fieldName>=<value>.
  Enclose all field-value pairs in one set of double quotation marks, delimited by spaces.
  Enclose values that contain spaces in single quotes.

  To get data on API performance metrics, specify both --perflog and --json.

  Examples:
```
sfdx force:data:record:update -s Account -i 001D000000Kv3dl -v "Name=NewAcme"
sfdx force:data:record:update -s Account -w "Name='Old Acme'" -v "Name='New Acme'"
sfdx force:data:record:update -s Account -i 001D000000Kv3dl -v "Name='Acme III' Website=www.example.com"
sfdx force:data:record:update -t -s TraceFlag -i 7tf170000009cUBAAY -v "ExpirationDate=2017-12-01T00:58:04.000+0000"
sfdx force:data:record:update -s Account -i 001D000000Kv3dl -v "Name=NewAcme" --perflog --json
```

<a id="force-data-soql-query" />

### `force:data:soql:query`

###### USAGE

```
sfdx force:data:soql:query -q <string> [-t] [-r human|csv|json] [--perflog] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -q, --query=query\
      (required) SOQL query to execute

  + -r, --resultformat=(human|csv|json)\
      [default: human] result format emitted to stdout; --json flag overrides this parameter

  + -t, --usetoolingapi\
      execute query with Tooling API

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --perflog\
      get API performance data

###### DESCRIPTION
  When you execute this command in a project, it executes the query against the data in your default scratch org.

  To get data on API performance metrics, specify both --perflog and --json.

  Examples:
  
```
sfdx force:data:soql:query -q "SELECT Id, Name, Account.Name FROM Contact"
sfdx force:data:soql:query -q "SELECT Id, Name FROM Account WHERE ShippingState IN ('CA', 'NY')"
sfdx force:data:soql:query -q "SELECT Name FROM ApexTrigger" -t
sfdx force:data:soql:query -q "SELECT Name FROM ApexTrigger" --perflog --json
```

<a id="force-data-tree-export" />

### `force:data:tree:export`

###### USAGE

```
sfdx force:data:tree:export -q <string> [-p] [-x <string>] [-d <directory>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --outputdir=outputdir\
      directory to store files

  + -p, --plan\
      generate mulitple sobject tree files and a plan definition file for
      aggregated import

  + -q, --query=query\
      (required) soql query, or filepath of file containing a soql query, to
      retrieve records

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -x, --prefix=prefix\
      prefix of generated files

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Generates JSON files for use with the force:data:tree:import command.

  Examples:
  
```
sfdx force:data:tree:export -q "SELECT Id, Name, (SELECT Name,Address__c FROM Properties__r) FROM Broker__c"
sfdx force:data:tree:export -q <path to file containing soql query> -x export-demo -d /tmp/sfdx-out -p
```

  For more information and examples, run "```sfdx force:data:tree:import -h```".

  The query for export can return a maximum of 2,000 records. For more information, see the REST API Developer Guide: 
  [https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_sobject_tree.htm](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_sobject_tree.htm)
  
  
<a id="force-data-tree-import" />

### `force:data:tree:import`

###### USAGE

```
sfdx force:data:tree:import [-f <array> | -p <filepath>] [--confighelp] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --sobjecttreefiles=sobjecttreefiles\
      comma-delimited, ordered paths of json files containing collection of record trees to insert

  + -p, --plan=plan\
      path to plan to insert multiple data files that have master-detail relationships

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --confighelp\
      display schema information for the --plan configuration file to stdout; if you use this option, all other OPTIONS except --json are ignored

###### DESCRIPTION
  To generate JSON files for use with force:data:tree:import, run "```sfdx force:data:tree:export```".

  Examples:

  To import records as individual files, first run the export commands:
  
```
sfdx force:data:tree:export -q "SELECT Id, Name FROM Account"
sfdx force:data:tree:export -q "SELECT Id, LastName, FirstName FROM Contact"
```
  Then run the import command:
```
sfdx force:data:tree:import -f Contact.json,Account.json -u me@my.org
```
  To import multiple data files as part of a plan, first run the export command with the -p | --plan flag:
```
sfdx force:data:tree:export -p -q "SELECT Id, Name, (SELECT Id, LastName, FirstName FROM Contacts) FROM Account"
```
  Then run the import command, supplying a filepath value for the -p | --plan parameter:
```
sfdx force:data:tree:import -p Account-Contact-plan.json -u me@my.org
```

  The SObject Tree API supports requests that contain up to 200 records. For more information, see the REST API Developer Guide:
  [https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_sobject_tree.htm](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_sobject_tree.htm)
  
<a id="force-doc-commands-display" />

### `force:doc:commands:display`

###### USAGE

```
sfdx force:doc:commands:display
```

###### DESCRIPTION
  Displays --help output for commands in the force namespace.
  To display more details about the commands’ parameters, include the --json flag.
  
<a id="force-doc-commands-list" />

### `force:doc:commands:list`

###### USAGE

```
sfdx force:doc:commands:list [-u]
```

###### OPTIONS
  + -u, --usage\
      list only docopt usage strings
	  
###### DESCRIPTION
  Displays a list of commands in the force namespace and their descriptions.

<a id="force-lightning-app-create" />

### `force:lightning:app:create`

###### USAGE

```
sfdx force:lightning:app:create -n <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --appname=appname\
      (required) name of the generated Lightning app

  + -t, --template=DefaultLightningApp\
      [default: DefaultLightningApp] template to use for file creation



###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values. The outputdir can be an absolute path or relative to the current working directory.
  If you don’t specify an outputdir, we create a subfolder in your current working directory with the name of your bundle. For example, if the current directory is force-app and your Lightning bundle is called myBundle, we create force-app/myBundle/ to store the files in the bundle.

  Examples:
  
```
sfdx force:lightning:app:create -n myapp
sfdx force:lightning:app:create -n myapp -d aura
```

<a id="force-lightning-component-create" />

### `force:lightning:component:create`

###### USAGE

```
sfdx force:lightning:component:create -n <string> [-t <string>] [-d <string>] [--type <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --componentname=componentname\
      (required) name of the generated Lightning component

  + -t, --template=DefaultLightningCmp\
      [default: DefaultLightningCmp] template to use for file creation

  + --type=aura|lwc\
      [default: aura] type of the Lightning component

###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.
  If you don’t specify an outputdir, we create a subfolder in your current working directory with the name of your bundle. For example, if the current working directory is force-app and your Lightning bundle is called myBundle, we create force-app/myBundle/ to store the files in the bundle.

  To create a Lightning web component, pass --type lwc to the command. If you don’t include a --type value, Salesforce CLI creates an Aura component by default.
  Examples:
  
```
sfdx force:lightning:component:create -n mycomponent
sfdx force:lightning:component:create -n mycomponent --type lwc
sfdx force:lightning:component:create -n mycomponent -d aura
sfdx force:lightning:component:create -n mycomponent --type lwc -d lwc
```

<a id="force-lightning-event-create" />

### `force:lightning:event:create`

###### USAGE

```
sfdx force:lightning:event:create -n <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --eventname=eventname\
      (required) name of the generated Lightning event

  + -t, --template=DefaultLightningEvt\
      [default: DefaultLightningEvt] template to use for file creation



###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.
  If you don’t specify an outputdir, we create a subfolder in your current working directory with the name of your bundle. For example, if the current working directory is force-app and your Lightning bundle is called myBundle, we create force-app/myBundle/ to store the files in the bundle.

  Examples:
  
```
sfdx force:lightning:event:create -n myevent
sfdx force:lightning:event:create -n myevent -d aura
```

<a id="force-lightning-interface-create" />

### `force:lightning:interface:create`

###### USAGE

```
sfdx force:lightning:interface:create -n <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --interfacename=interfacename\
      (required) name of the generated Lightning interface

  + -t, --template=DefaultLightningIntf\
      [default: DefaultLightningIntf] template to use for file creation


###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.
  If you don’t specify an outputdir, we create a subfolder in your current working directory with the name of your bundle. For example, if the current working directory is force-app and your Lightning bundle is called myBundle, we create force-app/myBundle/ to store the files in the bundle.

  Examples:
  
```
sfdx force:lightning:interface:create -n myinterface
sfdx force:lightning:interface:create -n myinterface -d aura
```

<a id="force-lightning-lint" />

### `force:lightning:lint`

###### USAGE

```
sfdx force:lightning:lint [-i <string>] [--files <string>] [--config <string>] [--exit] [--verbose]
```

###### OPTIONS
  + -i, --ignore=ignore\
      pattern used to ignore some folders

  + --config=config\
      path to a custom ESLint configuration file

  + --exit\
      exit with error code 1 if there are lint issues

  + --files=files\
      pattern used to include specific files

  + --verbose\
      report warnings in addition to errors

EXAMPLE:

```
sfdx force:lightning:lint ./path/to/be/linted/
```

<a id="force-lightning-test-create" />

### `force:lightning:test:create`

###### USAGE

```
sfdx force:lightning:test:create -n <string> [-t <string>] [-d <string>]
```

###### OPTIONS
  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --testname=testname\
      (required) name of the generated Lightning test

  + -t, --template=DefaultLightningTest\
      [default: DefaultLightningTest] template to use for file creation


###### DESCRIPTION
  The outputdir can be an absolute path or relative to the current working directory.

  Examples:
  
```
sfdx force:lightning:test:create -n MyLightningTest
sfdx force:lightning:test:create -n MyLightningTest -d lightningTests
```

<a id="force-lightning-test-install" />

### `force:lightning:test:install`

###### USAGE

```
sfdx force:lightning:test:install [-w <minutes>] [-r <string>] [-t jasmine|mocha|full] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -r, --releaseversion=releaseversion\
      [default: latest] release version of Lightning Testing Service

  + -t, --packagetype=(jasmine|mocha|full)\
      [default: full] type of unmanaged package. 'full' option contains both jasmine and mocha, plus examples

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] number of minutes to wait for installation status

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:
  
```
sfdx force:lightning:test:install
sfdx force:lightning:test:install -w 0 -r v1.0
sfdx force:lightning:test:install -t jasmine
```

<a id="force-lightning-test-run" />

### `force:lightning:test:run`

###### USAGE

```
sfdx force:lightning:test:run [-a <string>] [-d <directory>] [-f <filepath>] [-o] [-t <number>] [-r human|tap|junit|json] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --appname=appname\
      name of your Lightning test application

  + -d, --outputdir=outputdir\
      directory path to store test run artifacts: for example, log files and test results

  + -f, --configfile=configfile\
      path to config file for the test

  + -o, --leavebrowseropen\
      leave browser open

  + -r, --resultformat=(human|tap|junit|json)\
      [default: human] result format emitted to stdout; --json flag overrides this parameter

  + -t, --timeout=timeout\
      [default: 60000] time (ms) to wait for results element in dom

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:
  
```
sfdx force:lightning:test:run
sfdx force:lightning:test:run -a tests -r human
sfdx force:lightning:test:run -f config/myConfigFile.json -d testResultFolder
```

<a id="force-limits-api-display" />

### `force:limits:api:display`

###### USAGE
```
sfdx force:limits:api:display [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  When you execute this command in a project, it provides limit information for your default scratch org.

  Examples:
  
```
sfdx force:limits:api:display
sfdx force:limits:api:display -u me@my.org
```

<a id="force-mdapi-convert" />

### `force:mdapi:convert`

###### USAGE
```
sfdx force:mdapi:convert -r <directory> [-d <directory>]
```

###### OPTIONS
  + -d, --outputdir=outputdir\
      the output directory to store the source–formatted files

  + -r, --rootdir=rootdir\
      (required) the root directory containing the Metadata API–formatted metadata

###### DESCRIPTION
  NOTE: This command must be run from within a project.
  To use Salesforce CLI to work with components that you retrieved via Metadata API, first convert your files from the metadata format to the source format using "```sfdx force:mdapi:convert```".
  To convert files from the source format back to the metadata format, so that you can deploy them using "```sfdx force:mdapi:deploy```", run "```sfdx force:source:convert```".

  Examples:

```
sfdx force:mdapi:convert -r path/to/metadata
sfdx force:mdapi:convert -r path/to/metadata -d path/to/outputdir
```

<a id="force-mdapi-deploy" />

### `force:mdapi:deploy`

###### USAGE
```
sfdx force:mdapi:deploy [-c] [-d <directory> | -f <filepath>] [-w <minutes>] [-l NoTestRun|RunSpecifiedTests|RunLocalTests|RunAllTestsInOrg] [-r <array>] [-o] [-g] [-q <id>] [-u <string>] [--apiversion <string>] [--verbose]
```
###### OPTIONS
  + -c, --checkonly\
      validate deploy but don’t save to the org

  + -d, --deploydir=deploydir\
      root of directory tree of files to deploy

  + -f, --zipfile=zipfile\
      path to .zip file of metadata to deploy

  + -g, --ignorewarnings\
      whether a warning will allow a deployment to complete successfully

  + -l, --testlevel=(NoTestRun|RunSpecifiedTests|RunLocalTests|RunAllTestsInOrg)\
      deployment testing level

  + -o, --ignoreerrors\
      ignore any errors and do not roll back deployment

  + -q, --validateddeployrequestid=validateddeployrequestid\
      request ID of the validated deployment to run a Quick Deploy

  + -r, --runtests=runtests\
      tests to run if --testlevel RunSpecifiedTests

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      wait time for command to finish in minutes (default: 0)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      verbose output of deploy results

###### DESCRIPTION
  Specify the location of the files to deploy as a .zip file or by the root of the directory tree containing the files. To check the status of a deployment, specify its job ID. To run quick deploy of a recently validated package, use --validateddeployrequestid with the validated ID.
  To wait for the command to finish running no matter how long the deployment takes, set --wait to -1: "```sfdx force mdapi:deploy -w -1 ...```".
  

<a id="force-mdapi-deploy-cancel" />

### `force:mdapi:deploy:cancel`

###### USAGE

```
sfdx force:mdapi:deploy:cancel [-w <minutes>] [-i <id>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --jobid=jobid\
      job ID of the deployment you want to cancel; defaults to your most recent CLI deployment if not specified

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes 33

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Use this command to cancel a specified asynchronous metadata deployment. You can also specify a wait time (in minutes) to check for updates to the canceled deploy status.

  Examples:
  
  Deploy a directory of files to the org
```
sfdx force:mdapi:deploy -d <directory>
```
  Now cancel this deployment and wait two minutes
```
sfdx force:mdapi:deploy:cancel -w 2
```
  If you have multiple deployments in progress and want to cancel a specific one, specify the job ID
```
sfdx force:mdapi:deploy:cancel -i <jobid>
```
  Check the status of the cancel job
```
sfdx force:mdapi:deploy:report
```

<a id="force-mdapi-deploy-report" />

### `force:mdapi:deploy:report`

###### USAGE
```
sfdx force:mdapi:deploy:report [-w <minutes>] [-i <id>] [-u <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -i, --jobid=jobid\
      job ID of the deployment you want to check; defaults to your most recent CLI deployment if not specified

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      wait time for command to finish in minutes (default: 0)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command
	  
  + --verbose\
      verbose output of deploy results

###### DESCRIPTION
  Specify the job ID for the deploy you want to check. You can also specify a wait time (minutes) to check for updates to the deploy status.

<a id="force-mdapi-describemetadata" />

### `force:mdapi:describemetadata`

###### USAGE
```
sfdx force:mdapi:describemetadata [-f <filepath>] [-u <string>] [-a <string>]
```

###### OPTIONS
  + -a, + --apiversion=apiversion\\
      API version to use (the default is 46.0)

  + -f, --resultfile=resultfile\
      path to the file where results are stored

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

###### DESCRIPTION
  The default target username is the admin user for the default scratch org. The username must have the Modify All Data permission or the Modify Metadata permission (Beta). For more information about permissions, see Salesforce Help.

  Examples:

```
sfdx force:mdapi:describemetadata -a 43.0
sfdx force:mdapi:describemetadata -u me@example.com
sfdx force:mdapi:describemetadata -f /path/to/outputfilename.txt
sfdx force:mdapi:describemetadata -u me@example.com -f /path/to/outputfilename.txt
```

<a id="force-mdapi-listmetadata" />

### `force:mdapi:listmetadata`

###### USAGE
```
sfdx force:mdapi:listmetadata -m <string> [-f <filepath>] [--folder <string>] [-u <string>] [-a <string>]
```

###### OPTIONS
  + -a, + --apiversion=apiversion\\
      API version to use (the default is 46.0)

  + -f, --resultfile=resultfile\
      path to the file where results are stored

  + -m, --metadatatype=metadatatype\
      (required) metadata type to be retrieved, such as CustomObject; metadata type value is case-sensitive

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --folder=folder\
      folder associated with the component; required for components that use folders; folder names are case-sensitive

###### DESCRIPTION
  The default target username is the admin user for the default scratch org.

  Examples:
  
```
sfdx force:mdapi:listmetadata -m CustomObject
sfdx force:mdapi:listmetadata -m CustomObject -a 43.0
sfdx force:mdapi:listmetadata -m CustomObject -u me@example.com
sfdx force:mdapi:listmetadata -m CustomObject -f /path/to/outputfilename.txt
sfdx force:mdapi:listmetadata -m Dashboard --folder foldername
sfdx force:mdapi:listmetadata -m Dashboard --folder foldername -a 43.0
sfdx force:mdapi:listmetadata -m Dashboard --folder foldername -u me@example.com
sfdx force:mdapi:listmetadata -m Dashboard --folder foldername -f /path/to/outputfilename.txt
sfdx force:mdapi:listmetadata -m CustomObject -u me@example.com -f /path/to/outputfilename.txt
```

<a id="force-mdapi-retrieve" />

### `force:mdapi:retrieve`

###### USAGE

```
sfdx force:mdapi:retrieve -r <directory> [-w <minutes>] [-k <filepath>] [-d <directory>] [-p <array>] [-s] [-u <string>] [-a <string>] [--verbose]
```

###### OPTIONS
  + -a, + --apiversion=apiversion\\
      target API version for the retrieve (default 46.0)

  + -d, --sourcedir=sourcedir\
      source dir to use instead of the default package dir in sfdx-project.json

  + -k, --unpackaged=unpackaged\
      file path of manifest of components to retrieve

  + -p, --packagenames=packagenames\
      a comma-separated list of packages to retrieve

  + -r, --retrievetargetdir=retrievetargetdir\
      (required) directory root for the retrieved files

  + -s, --singlepackage\
      a single-package retrieve (default: false)

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      wait time for command to finish in minutes (default: -1 (no limit))

  + --verbose\
      verbose output of retrieve result

###### DESCRIPTION
  The default target username is the admin user for the default scratch org. You can retrieve and deploy up to 10,000 files or 400 MB (39 MB compressed) at one time.
  
<a id="force-mdapi-retrieve-report" />

### `force:mdapi:retrieve:report`

###### USAGE
```
sfdx force:mdapi:retrieve:report [-w <minutes>] [-r <directory>] [-i <id>] [-u <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -i, --jobid=jobid\
      job ID of the retrieve you want to check; defaults to your most recent CLI retrieval if not specified

  + -r, --retrievetargetdir=retrievetargetdir\
      directory root for the retrieved files

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      wait time for command to finish in minutes (default: -1 (no limit))

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      verbose output of retrieve result

###### DESCRIPTION
  Specify the job ID and a target directory for the retrieve you want to check.
  You can also specify a wait time (minutes) to check for updates to the deploy status. If the retrieve was successful, the resulting zip file will be saved to the location passed in with the retrieve target parameter.

<a id="force-org-clone" />

### `force:org:clone`

###### USAGE
```
sfdx force:org:clone [name=value...] -t sandbox [-f <filepath>] [-s] [-a <string>] [-w <minutes>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      alias for the created org

  + -f, --definitionfile=definitionfile\
      path to an org definition file

  + -s, --setdefaultusername\
      set the created org as the default username

  + -t, --type=(sandbox)\
      (required) type of org to create

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] the streaming client socket timeout (in minutes)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

<a id="force-org-create" />

### `force:org:create`

###### USAGE
```
sfdx force:org:create [name=value...] [-t scratch|sandbox] [-f <filepath>] [-n] [-c] [-i <string>] [-s] [-a <string>] [-w <minutes>] [-d <number>] [-v <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      alias for the created org

  + -c, --noancestors\
      do not include second-generation package ancestors in the scratch org

  + -d, --durationdays=durationdays\
      duration of the scratch org (in days) (default:7, min:1, max:30)

  + -f, --definitionfile=definitionfile\
      path to an org definition file

  + -i, --clientid=clientid\
      connected app consumer key; not supported for sandbox org creation

  + -n, --nonamespace\
      create the scratch org with no namespace

  + -s, --setdefaultusername\
      set the created org as the default username

  + -t, --type=(scratch|sandbox)\
      [default: scratch] type of org to create; sandbox org creation is in beta

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + -w, --wait=wait\
      [default: [object Object]] the streaming client socket timeout (in minutes)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  To set up a connected app for your new org, specify the value that was returned when you created a connected app in your Dev Hub/Production org as --clientid.

  Examples:
  
```
sfdx force:org:create -f config/enterprise-scratch-def.json -a TestOrg1
sfdx force:org:create -a MyDevOrg -s -v me@myhub.org edition=Developer
sfdx force:org:create -f config/enterprise-scratch-def.json -a OrgWithOverrides username=testuser1@mycompany.org
```

<a id="force-org-delete" />

### `force:org:delete`

###### USAGE
```
sfdx force:org:delete [-p] [-v <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -p, --noprompt\
      no prompt to confirm deletion

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  To mark the org for deletion without being prompted to confirm, specify --noprompt.

  Examples:
  
```
sfdx force:org:delete -u me@my.org
sfdx force:org:delete -u MyOrgAlias -p
```

<a id="force-org-display" />

### `force:org:display`

###### USAGE
```
sfdx force:org:display [-u <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      emit additional command output to stdout

###### DESCRIPTION
  Output includes your access token, client ID, connected status, org ID, instance URL, username, and alias, if applicable.
  Use --verbose to include the SFDX auth URL. Including --verbose displays the sfdxAuthUrl property only if you authenticated to the org using force:auth:web:login (not force:auth:jwt:grant).

  Examples:
  
```
sfdx force:org:display
sfdx force:org:display -u me@my.org
sfdx force:org:display -u TestOrg1 --json
sfdx force:org:display -u TestOrg1 --json > tmp/MyOrgDesc.json
```

<a id="force-org-list" />

### `force:org:list`

###### USAGE
```
sfdx force:org:list [--all] [--clean] [-p] [--verbose]
```

###### OPTIONS
  + -p, --noprompt\
      do not prompt for confirmation

  + --all\
      include expired, deleted, and unknown-status scratch orgs

  + --clean\
      remove all local org authorizations for non-active orgs

  + --verbose\
      list more information about each org

###### DESCRIPTION
  Examples:
```
sfdx force:org:list
sfdx force:org:list --verbose --json
sfdx force:org:list --verbose --json > tmp/MyOrgList.json
```

<a id="force-org-open" />

### `force:org:open`

###### USAGE
```
sfdx force:org:open [-p <string>] [-r] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -p, --path=path\
      navigation URL path

  + -r, --urlonly\
      display navigation URL, but don’t launch browser

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Opens your default scratch org, or another org that you specify.
  To open a specific page, specify the portion of the URL after "yourInstance.salesforce.com/" as --path.
  For example, specify "```--path lightning```" to open Lightning Experience, or specify "```--path /apex/YourPage```" to open a Visualforce page.

  To generate a URL but not launch your browser, specify --urlonly.

  Examples:
  
```
sfdx force:org:open
sfdx force:org:open -u me@my.org
sfdx force:org:open -u MyTestOrg1
sfdx force:org:open -r -p lightning
```

<a id="force-org-shape-create" />

### `force:org:shape:create`

###### USAGE
```
sfdx force:org:shape:create [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command


###### DESCRIPTION
  Examples:

```
sfdx force:org:shape:create -u me@my.org
sfdx force:org:shape:create -u me@my.org --json --loglevel debug
```

<a id="force-org-shape-delete" />

### `force:org:shape:delete`

###### USAGE
```
sfdx force:org:shape:delete [-p] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -p, --noprompt\
      do not prompt for confirmation

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  
###### DESCRIPTION
  Examples:

```
sfdx force:org:shape:delete -u me@my.org
sfdx force:org:shape:delete -u MyOrgAlias -p
sfdx force:org:shape:delete -u me@my.org --json
sfdx force:org:shape:delete -u me@my.org -p --json > tmp/MyOrgShapeDelete.json
```

<a id="force-org-shape-list" />

### `force:org:shape:list`

###### USAGE
```
sfdx force:org:shape:list [--verbose]
```

###### OPTIONS

  + --verbose\
      list more information about each org shape

###### DESCRIPTION
  Examples:

```
sfdx force:org:shape:list
sfdx force:org:shape:list --json
sfdx force:org:shape:list --json > tmp/MyOrgShapeList.json
```

<a id="force-org-snapshot-create" />

### `force:org:snapshot:create`

###### USAGE
```
sfdx force:org:snapshot:create -o <string> -n <string> [-d <string>] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --description=description\
      description of snapshot

  + -n, --snapshotname=snapshotname\
      (required) unique name of snapshot

  + -o, --sourceorg=sourceorg\
      (required) ID or locally authenticated username or alias of scratch org to snapshot

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  A snapshot is a point-in-time export of a scratch org. The export is stored in Salesforce and referenced by its unique name in a scratch definition file.
  Use "```sfdx force:org:snapshot:get```" to get details, including status, about a snapshot creation request.
  With "snapshot" in your scratch org definition file, use "```sfdx force:org:create```" to create a scratch org from a snapshot.

  Examples:

```
sfdx force:org:snapshot:create --sourceorg 00Dxx0000000000 --snapshotname Dependencies --description "Contains PackageA v1.1.0"
sfdx force:org:snapshot:create -o myuser@myorg -n NightlyBranch -d "Contains PkgA v2.1.0 and PkgB 3.3.0"
```

<a id="force-org-snapshot-delete" />

### `force:org:snapshot:delete`

###### USAGE
```
sfdx force:org:snapshot:delete -s <string> [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -s, --snapshot=snapshot\
      (required) name or ID of snapshot to delete

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:
  
```
sfdx force:org:snapshot:delete --snapshot 0Oo...
sfdx force:org:snapshot:delete -s BaseSnapshot
```

<a id="force-org-snapshot-get" />

### `force:org:snapshot:get`

###### USAGE
```
sfdx force:org:snapshot:get -s <string> [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -s, --snapshot=snapshot\
      (required) name or ID of snapshot to retrieve

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Use "```sfdx force:org:snapshot:create```" to create a snapshot.

  Use "```sfdx force:org:snapshot:list```" to retrieve all snapshots.

  Examples:
```
sfdx force:org:snapshot:get --snapshot 0Oo...
sfdx force:org:snapshot:get -s Dependencies
```

<a id="force-org-snapshot-list" />

### `force:org:snapshot:list`

###### USAGE
```
sfdx force:org:snapshot:list [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Use "```sfdx force:org:snapshot:get```" to get details about a snapshot request.
  Use "```sfdx force:org:snapshot:create```" to create a snapshot.

  Examples:
  
```
sfdx force:org:snapshot:list
sfdx force:org:snapshot:list -v OtherDevHub@example.com
```

<a id="force-org-status" />

### `force:org:status`

###### USAGE
```
sfdx force:org:status -n <string> [-s] [-a <string>] [-w <minutes>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      alias for the created org

  + -n, --sandboxname=sandboxname\
      (required) name of the sandbox org to check status for

  + -s, --setdefaultusername\
      set the created org as the default username

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] number of minutes to wait while polling for status

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  
<a id="force-package1-version-create" />

### `force:package1:version:create`

###### USAGE
```
sfdx force:package1:version:create -i <id> -n <string> [-d <string>] [-v <string>] [-m] [-r <url>] [-p <url>] [-k <string>] [-w <number>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --description=description\
      package version description

  + -i, --packageid=packageid\
      (required) ID of the metadata package (starts with 033) of which you’re creating a new version

  + -k, --installationkey=installationkey\
      installation key for key-protected package (default: null)

  + -m, --managedreleased\
      create a managed package version

  + -n, --name=name\
      (required) package version name

  + -p, --postinstallurl=postinstallurl\
      post install URL

  + -r, --releasenotesurl=releasenotesurl\
      release notes URL

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --version=version\
      package version in major.minor format, for example, 3.2

  + -w, --wait=wait\
      minutes to wait for the package version to be created (default: 2 minutes)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  The package version is based on the contents of the specified metadata package. Omit -m if you want to create an unmanaged package version.

<a id="force-package1-version-create-get" />

### `force:package1:version:create:get`

###### USAGE

```
sfdx force:package1:version:create:get -i <id> [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --requestid=requestid\
      (required) PackageUploadRequest ID

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:
  
```
sfdx force:package:version:create:report -i 08c...
sfdx force:package:version:create:report -i 08c... -v devhub@example.com
```

<a id="force-package1-version-display" />

### `force:package1:version:display`

###### USAGE
```
sfdx force:package1:version:display -i <id> [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --packageversionid=packageversionid\
      (required) metadata package version ID (starts with 04t)

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Display detailed information about an individual package version, including metadata package ID, name, the release state, and build number.

<a id="force-package1-version-list" />

### `force:package1:version:list`

###### USAGE
```
sfdx force:package1:version:list [-i <id>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --packageid=packageid\
      metadata package ID (starts with 033)

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  If a metadata package ID is specified, lists all versions of the specified package. Otherwise, lists all package versions for the org. For each package version, the list includes the package version ID, metadata package ID, name, version number, and release state.

<a id="force-package-create" />

### `force:package:create`

###### USAGE
```
sfdx force:package:create -n <string> -t Managed|Unlocked -r <directory> [-d <string>] [-e] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --description=description\
      package description

  + -e, --nonamespace\
      creates the package with no namespace; available only for unlocked packages.

  + -n, --name=name\
      (required) package name

  + -r, --path=path\
      (required) path to directory that contains the contents of the package

  + -t, --packagetype=(Managed|Unlocked)\
      (required) package type

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.
  First, use this command to create a package. Then create a package version.
  If you don’t have a namespace defined in your sfdx-project.json file, use --nonamespace.
  Your --name value must be unique within your namespace.

  Examples:
  
```
sfdx force:package:create -n YourPackageName -t Unlocked -r force-app
sfdx force:package:create -n YourPackageName -d "Your Package Descripton" -t Unlocked -r force-app
```
  Run '```sfdx force:package:list```' to list all packages in the Dev Hub org.
  
<a id="force-package-hammertest-list" />

### `force:package:hammertest:list`

###### USAGE
```
sfdx force:package:hammertest:list [-i <id>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --packageversionid=packageversionid\
      ID of the package version to list results for

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.
  If you supply a --packageversionid value, this command returns test statuses for only the tests associated with the specified package version. If you don’t include the --packageversionid parameter, the command lists all test statuses.

  Examples:
```
sfdx force:package:hammertest:list -u you@yourpackagingorg.com -i 04t...
sfdx force:package:hammertest:list -u you@yourpackagingorg.com
```

<a id="force-package-hammertest-report" />

### `force:package:hammertest:report`

###### USAGE
```
sfdx force:package:hammertest:report -i <id> [-s] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --requestid=requestid\
      (required) ID of the hammer request to report on

  + -s, --summary\
      report only a results summary (hide Apex test failures)

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Example:
```
sfdx force:package:hammertest:report -u you@yourpackagingorg.com -i 0TW...
```

<a id="force-package-hammertest-run" />

### `force:package:hammertest:run`

###### USAGE
```
sfdx force:package:hammertest:run -i <array> [-s <array>] [-f <string>] [-d <string>] [-p] [-t] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --scheduledrundatetime=scheduledrundatetime\
      earliest date/time to run the package upgrade test (YYYY-MM-DD HH:mm:ss, in GMT)

  + -f, --subscriberfile=subscriberfile\
      file with list of subscriber orgs IDs, one per line

  + -i, --packageversionids=packageversionids\
      (required) comma-separated list of package version IDs to test

  + -p, --preview\
      run the package hammer test in the Salesforce preview version

  + -s, --subscriberorgs=subscriberorgs\
      comma-separated list of subscriber org IDs

  + -t, --apextests\
      after package upgrade validation, run the package's Apex tests in the subscriber org

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Use this command to run ISV Hammer for the specified package versions and subscriber orgs.
  If Salesforce has enabled Multiple Managed Packages for your org, you can test more than one package version. Supply the IDs of the package versions you want to test in the desired order of execution.
  The command creates a copy of each of the supplied subscriber orgs and tests the package upgrade in each of them.
  If a scheduled date/time is supplied, validation and setup start immediately but the package upgrade test will not start until after the supplied date/time. Format the --scheduledrundatetime value as YYYY-MM-DD HH:mm:ss in the GMT timezone. This date cannot be more than 25 days from today.
  To test against the Salesforce preview release version, during the sandbox preview window, include --preview and a --scheduledrundatetime value that’s immediately after a staggered release, based on the Salesforce release calendar.
  To run the package version’s Apex tests in each subscriber org after successfully testing the package upgrade, include --apextests.
  The command returns a request ID (starts with 0TW). Use this IsvHammerRequest
  ID to query for the test status by running "```sfdx force:package:hammertest:report -i 0TW...```".

  Examples:
```
sfdx force:package:hammertest:run -u you@yourpackagingorg.com -i 04t...a,04t...b -s 00D...a,00Dx...b
sfdx force:package:hammertest:run -u you@yourpackagingorg.com -i 04t... -f subscriberOrgs.txt
```

<a id="force-package-install" />

### `force:package:install`

###### USAGE
```
sfdx force:package:install [-w <minutes>] [-k <string>] [-b <minutes>] [-r] [-p <string>] [-a all|package] [-s AllUsers|AdminsOnly] [-t DeprecateOnly|Mixed|Delete] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --apexcompile=(all|package)\
      [default: all] compile all Apex in the org and package, or only Apex in the package

  + -b, --publishwait=publishwait\
      number of minutes to wait for subscriber package version ID to become available in the target org

  + -k, --installationkey=installationkey\
      installation key for key-protected package (default: null)

  + -p, --package=package\
      ID (starts with 04t) or alias of the package version to install

  + -r, --noprompt\
      do not prompt for confirmation

  + -s, --securitytype=(AllUsers|AdminsOnly)\
      [default: AllUsers] security access type for the installed package (deprecation notice: The default --securitytype value will change from AllUsers to AdminsOnly in v47.0 or later.)

  + -t, --upgradetype=(DeprecateOnly|Mixed|Delete)\
      [default: Mixed] the upgrade type for the package installation

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      number of minutes to wait for installation status

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Supply the ID of the package version to install. The package installs in your default target org unless you supply the username for a different target org.
  For package upgrades, to specify options for component deprecation or deletion of removed components, include an --upgradetype value. To delete components that can be safely deleted and deprecate the others, specify --upgradetype
  Mixed (the default). To deprecate all removed components, specify --upgradetype DeprecateOnly. To delete all removed components, except for custom objects and custom fields, that don't have dependencies, specify --upgradetype Delete. (Note: This option can result in the loss of data that is associated with the deleted components.) The default is Mixed.

  Examples:
```
sfdx force:package:install --package 04t... -u me@example.com
sfdx force:package:install --package awesome_package_alias
sfdx force:package:install --package "Awesome Package Alias"
sfdx force:package:install --package 04t... -t DeprecateOnly
```

<a id="force-package-install-report" />

### `force:package:install:report`

###### USAGE
```
sfdx force:package:install:report -i <id> [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --requestid=requestid\
      (required) ID of the package install request you want to check

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION

  Examples:

```
sfdx force:package:install:report -i 0Hf...
sfdx force:package:install:report -i 0Hf... -u me@example.com
```

<a id="force-package-installed-list" />

### `force:package:installed:list`

###### USAGE
```
sfdx force:package:installed:list [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Examples:

```
sfdx force:package:installed:list
sfdx force:package:installed:list -u me@example.com
```

<a id="force-package-list" />

### `force:package:list`

###### USAGE

```
sfdx force:package:list [-v <string>] [--apiversion <string>] [--verbose]
```
 

###### OPTIONS
  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      display extended package detail

###### DESCRIPTION
  You can view the namespace, IDs, and other details for each package.

  Examples:
  
```
sfdx force:package:list -v devhub@example.com
sfdx force:package:list -v devhub@example.com --verbose
```

<a id="force-package-uninstall" />

### `force:package:uninstall`

###### USAGE
```
sfdx force:package:uninstall [-w <minutes>] [-p <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -p, --package=package\
      ID (starts with 04t) or alias of the package version to uninstall

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      number of minutes to wait for uninstall status

  + --apiversion=apiversion\
      override the api version used for api requests made by this command


###### DESCRIPTION
  Specify the package ID for a second-generation package.

  Examples:

```
sfdx force:package:uninstall -p 04t... -u me@example.com
sfdx force:package:uninstall -p undesirable_package_alias
sfdx force:package:uninstall -p "Undesirable Package Alias"
```

  To list the org’s installed packages, run "```sfdx force:package:installed:list```".

  To uninstall a first-generation package, from Setup, enter Installed Packages in the Quick Find box, then select Installed Packages.
  
<a id="force-package-uninstall-report" />

### `force:package:uninstall:report`

###### USAGE
```
sfdx force:package:uninstall:report -i <id> [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --requestid=requestid\
      (required) ID of the package uninstall request you want to check

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:

```
sfdx force:package:uninstall:report -i 06y...
sfdx force:package:uninstall:report -i 06y... -u me@example.com
```

<a id="force-package-update" />

### `force:package:update`

###### USAGE
```
sfdx force:package:update -p <string> [-n <string>] [-d <string>] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -d, --description=description\
      new package description

  + -n, --name=name\
      new package name

  + -p, --package=package\
      (required) ID (starts with 0Ho) or alias of the package to update

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Specify a new value for each option you want to update.

  Examples:
  
```
sfdx force:package:update -p "Your Package Alias" -n "New Package Name"
sfdx force:package:update -p 0Ho... -d "New Package description"
```

  Run "```sfdx force:package:list```" to list all packages in the Dev Hub org.
  
<a id="force-package-version-create" />

### `force:package:version:create`

###### USAGE
```
sfdx force:package:version:create [-p <string>] [-d <directory>] [-f <filepath>] [-b <string>] [-t <string>] [-k <string>] [-x] [-w <minutes>] [-a <string>] [-n <string>] [-e <string>] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --versionname=versionname\
      the name of the package version to be created

  + -b, --branch=branch\
      the package version’s branch

  + -d, --path=path\
      path to directory that contains the contents of the package

  + -e, --versiondescription=versiondescription\
      the description of the package version to be created

  + -f, --definitionfile=definitionfile\
      path to a definition file similar to scratch org definition file that contains the list of features and org preferences that the metadata of the package version depends on

  + -k, --installationkey=installationkey\
      installation key for key-protected package (either --installationkey or --installationkeybypass is required)

  + -n, --versionnumber=versionnumber\
      the version number of the package version to be created

  + -p, --package=package\
      ID (starts with 0Ho) or alias of the package to create a version of

  + -t, --tag=tag\
      the package version’s tag

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + -w, --wait=wait\
      [default: [object Object]] minutes to wait for the package version to be created

  + -x, --installationkeybypass\
      bypass the installation key requirement (either --installationkey or --installationkeybypass is required)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.
  The package version is based on the package contents in the specified directory.
  To retrieve details about a package version create request, including status and package version ID (04t), run "```sfdx force:package:version:create:report -i 08c...```".
  We recommend specifying the --installationkey to protect the contents of your package and to prevent unauthorized installation of your package.
  To list package version creation requests in the org, run "```sfdx force:package:version:create:list```".

  Examples:
  
```
sfdx force:package:version:create -d common -k password123
sfdx force:package:version:create -p "Your Package Alias" -k password123
sfdx force:package:version:create -p 0Ho... -k password123
```

<a id="force-package-version-create-list" />

### `force:package:version:create:list`

###### USAGE
```
sfdx force:package:version:create:list [-c <number>] [-s Queued|InProgress|Success|Error] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -c, --createdlastdays=createdlastdays\
      created in the last specified number of days (starting at 00:00:00 of first day to now; 0 for today)

  + -s, --status=(Queued|InProgress|Success|Error)\
      filter the list by version creation request status

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Shows the details of each request to create a package version in the Dev Hub org.
  All filter parameters are applied using the AND logical operator (not OR).
  To get information about a specific request, run "```sfdx force:package:version:create:report```" and supply the request ID.

  Examples:
  
```
sfdx force:package:version:create:list
sfdx force:package:version:create:list --createdlastdays 3
sfdx force:package:version:create:list --status Error
sfdx force:package:version:create:list -s InProgress
sfdx force:package:version:create:list -c 3 -s Success
```

<a id="force-package-version-create-report" />

### `force:package:version:create:report`

###### USAGE
```
sfdx force:package:version:create:report -i <id> [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --packagecreaterequestid=packagecreaterequestid\
      (required) package version creation request ID (starts with 08c)

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Specify the request ID for which you want to view details. If applicable, the command displays errors related to the request.

  Examples:
  
```
sfdx force:package:version:create:report -i 08c...
sfdx force:package:version:create:report -i 08c... -v devhub@example.com
```

  To show all requests in the org, run "```sfdx force:package:version:create:list```".

<a id="force-package-version-list" />

### `force:package:version:list`

###### USAGE
```
sfdx force:package:version:list [-c <number>] [-m <number>] [-p <array>] [-r] [-o <array>] [-v <string>] [--apiversion <string>] [--concise] [--verbose]
```

###### OPTIONS
  + -c, --createdlastdays=createdlastdays\
      created in the last specified number of days (starting at 00:00:00 of first day to now; 0 for today)

  + -m, --modifiedlastdays=modifiedlastdays\
      list items modified in the specified last number of days (starting at 00:00:00 of first day to now; 0 for today)

  + -o, --orderby=orderby\
      order by the specified package version fields

  + -p, --packages=packages\
      filter results on specified comma-delimited packages (aliases or 0Ho IDs)

  + -r, --released\
      display released versions only

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --concise\
      display limited package version details

  + --verbose\
      display extended package version details

###### DESCRIPTION
  Displays details of each package version in the org.
  Use --concise or --verbose to display limited or additional details, respectively.
  All filter parameters are applied using the AND logical operator (not OR).

  Examples:
  
```
sfdx force:package:version:list --verbose --createdlastdays 3 --released --orderby PatchVersion
sfdx force:package:version:list --packages 0Ho000000000000,0Ho000000000001 --released --modifiedlastdays 0
sfdx force:package:version:list --released
sfdx force:package:version:list --concise --modifiedlastdays 0
sfdx force:package:version:list --concise -c 3 -r
sfdx force:package:version:list --packages exp-mgr,exp-mgr-util --released --modifiedlastdays 0
```

<a id="force-package-version-promote" />

### `force:package:version:promote`

###### USAGE
```
sfdx force:package:version:promote -p <string> [-n] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -n, --noprompt\
      no prompt to confirm setting the package version as released

  + -p, --package=package\
      (required) ID (starts with 04t) or alias of the package version to promote

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Supply the ID or alias of the package version you want to promote. Promotes the package version to released status.

  Examples:
  
```
sfdx force:package:version:promote -p 04t...
sfdx force:package:version:promote -p awesome_package_alias
sfdx force:package:version:promote -p "Awesome Package Alias"
```

<a id="force-package-version-report" />

### `force:package:version:report`

###### USAGE
```
sfdx force:package:version:report -p <string> [-v <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -p, --package=package\
      (required) ID (starts with 04t) or alias of the package to retrieve details for

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      displays extended package version details

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Examples:
  
```
sfdx force:package:version:report -p 04t...
sfdx force:package:version:report -p "Your Package Alias"
```

  To update package version values, run "```sfdx force:package:version:update```".

<a id="force-package-version-update" />

### `force:package:version:update`

###### USAGE
```
sfdx force:package:version:update -p <string> [-a <string>] [-e <string>] [-b <string>] [-t <string>] [-k <string>] [-v <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --versionname=versionname\
      new package version name

  + -b, --branch=branch\
      new package version branch

  + -e, --versiondescription=versiondescription\
      new package version description

  + -k, --installationkey=installationkey\
      new installation key for key-protected package (default: null)

  + -p, --package=package\
      (required) ID (starts with 04t) or alias of the package to update a version of

  + -t, --tag=tag\
      new package version tag

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Specify a new value for each option you want to update.

  Examples:
  
```
sfdx force:package:version:update -p "Your Package Alias" -k password123
sfdx force:package:version:update -p 04t... -b master -t 'Release 1.0.7'
sfdx force:package:version:update -p 04t... -e "New Package Version description"
```

  To display details about a package version, run "```sfdx force:package:version:report```".
  
<a id="force-project-create" />

### `force:project:create`

###### USAGE
```
sfdx force:project:create -n <string> [-t <string>] [-d <string>] [-s <string>] [-p <string>] [-x]
```

###### OPTIONS
  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -n, --projectname=projectname\
      (required) name of the generated project

  + -p, --defaultpackagedir=defaultpackagedir\
      [default: force-app] default package directory name

  + -s, --namespace=namespace\
      project associated namespace

  + -t, --template=standard|empty\
      [default: standard] template to use for project creation

  + -x, --manifest\
      generate a manifest (package.xml) for change-set-based development



###### DESCRIPTION
  Default values are used if the template, namespace, defaultpackagedir, and outputdir aren’t supplied.
  The outputdir can be an absolute path or relative to the current working directory.

  Examples:

```
sfdx force:project:create --projectname mywork
sfdx force:project:create --projectname mywork --defaultpackagedir myapp
sfdx force:project:create --projectname mywork --defaultpackagedir myapp --manifest
sfdx force:project:create --projectname mywork --template empty
```

<a id="force-project-upgrade" />

### `force:project:upgrade`

###### USAGE

```
sfdx force:project:upgrade [-f]
```

###### OPTIONS
  + -f, --forceupgrade\
      run all upgrades even if project has already been upgraded

###### DESCRIPTION
  Examples:
  
```
sfdx force:project:upgrade
sfdx force:project:upgrade -f
```

<a id="force-schema-sobject-describe" />

### `force:schema:sobject:describe`

###### USAGE
```
sfdx force:schema:sobject:describe -s <string> [-t] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -s, --sobjecttype=sobjecttype\
      (required) the API name of the object to describe

  + -t, --usetoolingapi\
      execute with Tooling API

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Examples:
  
```
sfdx force:schema:sobject:describe -s Account
sfdx force:schema:sobject:describe -s MyObject__c
sfdx force:schema:sobject:describe -s ApexClass -t
```

<a id="force-schema-sobject-list" />

### `force:schema:sobject:list`

###### USAGE
```
sfdx force:schema:sobject:list -c <string> [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -c, --sobjecttypecategory=sobjecttypecategory\
      (required) the type of objects to list (all|custom|standard)

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Lists all objects, custom objects, or standard objects in the org.

  Examples:
  
```
sfdx force:schema:sobject:list -c all
sfdx force:schema:sobject:list -c custom
sfdx force:schema:sobject:list -c standard
```

<a id="force-source-convert" />

### `force:source:convert`

###### USAGE
```
sfdx force:source:convert [-r <directory>] [-d <directory>] [-n <string>]
```

###### OPTIONS
  + -d, --outputdir=outputdir\
      output directory to store the Metadata API–formatted files in

  + -n, --packagename=packagename\
      name of the package to associate with the metadata-formatted files

  + -r, --rootdir=rootdir\
      a source directory other than the default package to convert

###### DESCRIPTION
  NOTE: This command must be run from within a project.
  To convert source-formatted files into the metadata format, so that you can deploy them using Metadata API, run "```sfdx force:source:convert```". Then deploy the metadata using "```sfdx force:mdapi:deploy```".
  To convert Metadata API–formatted files into the source format, run "```sfdx force:mdapi:convert```".
  To specify a package name that includes spaces, enclose the name in single quotes.

  Examples:
```
sfdx force:source:convert -r path/to/source
sfdx force:source:convert -r path/to/source -d path/to/outputdir -n 'My Package'
```

<a id="force-source-delete" />

### `force:source:delete`

###### USAGE
```
sfdx force:source:delete [-r] [-w <minutes>] [-p <array> | -m <array>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -m, --metadata=metadata\
      comma-separated list of names of metadata components to delete

  + -p, --sourcepath=sourcepath\
      comma-separated list of paths to the local metadata to delete

  + -r, --noprompt\
      do not prompt for delete confirmation

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes 33

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Use this command to delete components from orgs that don’t have source tracking, such as sandboxes.
  To remove deleted items from scratch orgs, which have change tracking, use "```sfdx force:source:push```".

  Examples:
```
sfdx force:source:delete -p path/to/source
sfdx force:source:delete -m <metadata>
```

<a id="force-source-deploy" />

### `force:source:deploy`

###### USAGE
```
sfdx force:source:deploy [-w <minutes>] [-q <id> | -x <filepath> | -m <array> | -p <array> | -c | -l NoTestRun|RunSpecifiedTests|RunLocalTests|RunAllTestsInOrg | -r <array> | -o | -g] [-u <string>] [--apiversion <string>] [--verbose]
```

###### OPTIONS
  + -c, --checkonly\
      validate deploy but don’t save to the org

  + -g, --ignorewarnings\
      whether a warning will allow a deployment to complete successfully

  + -l, --testlevel=(NoTestRun|RunSpecifiedTests|RunLocalTests|RunAllTestsInOrg) deployment testing level\

  + -m, --metadata=metadata\
      comma-separated list of metadata component names

  + -o, --ignoreerrors\
      ignore any errors and do not roll back deployment

  + -p, --sourcepath=sourcepath\
      comma-separated list of paths to the local source files to deploy

  + -q, --validateddeployrequestid=validateddeployrequestid\
      request ID of the validated deployment to run a Quick Deploy

  + -r, --runtests=runtests\
      tests to run if --testlevel RunSpecifiedTests

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes

  + -x, --manifest=manifest\
      file path for manifest (package.xml) of components to deploy

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

  + --verbose\
      verbose output of deploy results

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Use this command to deploy source (metadata that’s in source format) to an org.
  To take advantage of change tracking with scratch orgs, use "```sfdx force:source:push```".
  To deploy metadata that’s in metadata format, use "```sfdx force:mdapi:deploy```".

  The source you deploy overwrites the corresponding metadata in your org. This command does not attempt to merge your source with the versions in your org.

  To run the command asynchronously, set --wait to 0, which immediately returns the job ID. This way, you can continue to use the CLI.
  To check the status of the job, use force:source:deploy:report.

  If the comma-separated list you’re supplying contains spaces, enclose the entire comma-separated list in one set of double quotes.

  Examples:
  
  To deploy the source files in a directory:
```
sfdx force:source:deploy -p path/to/source
```
  To deploy a specific Apex class and the objects whose source is in a directory:
```
sfdx force:source:deploy -p path/to/apex/classes/MyClass.cls,path/to/source/objects 
```
	To deploy source files in a comma-separated list that contains spaces:
```
sfdx force:source:deploy -p "path/to/objects/MyCustomObject/fields/MyField.field-meta.xml, path/to/apex/classes"
```
  To deploy all Apex classes:
```
sfdx force:source:deploy -m ApexClass
```
  To deploy a specific Apex class:
```
sfdx force:source:deploy -m ApexClass:MyApexClass
```
  To deploy all custom objects and Apex classes:
```
sfdx force:source:deploy -m CustomObject,ApexClass
```
  To deploy all Apex classes and two specific profiles (one of which has a space in its name):
```
sfdx force:source:deploy -m "ApexClass, Profile:My Profile, Profile: AnotherProfile"
```
  To deploy all components listed in a manifest:
```
sfdx force:source:deploy -x path/to/package.xml
```
  To run the tests that aren’t in any managed packages as part of a deployment:
```
sfdx force:source:deploy -m ApexClass -l RunLocalTests
```
  To check whether a deployment would succeed (to prepare for Quick Deploy):
```
sfdx force:source:deploy -m ApexClass -l RunAllTestsInOrg -c
```
  To deploy an already validated deployment (Quick Deploy):
```
sfdx force:source:deploy -q 0Af9A00000FTM6pSAH
```

<a id="force-source-deploy-cancel" />

### `force:source:deploy:cancel`

###### USAGE
```
sfdx force:source:deploy:cancel [-w <minutes>] [-i <id>] [-u <string>] [--apiversion <string>]
```
###### OPTIONS
  + -i, --jobid=jobid\
      job ID of the deployment you want to cancel; defaults to your most recent CLI deployment if not specified

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes 33

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Use this command to cancel a specified asynchronous source deployment. You can also specify a wait time (in minutes) to check for updates to the canceled deploy status.

  To run the command asynchronously, set --wait to 0, which immediately returns the job ID. This way, you can continue to use the CLI.
  To check the status of the job, use force:source:deploy:report.

  Examples:
  
Deploy a directory of files to the org
```
sfdx force:source:deploy -d <directory>
```
  Now cancel this deployment and wait two minutes
```
sfdx force:source:deploy:cancel -w 2
```

  If you have multiple deployments in progress and want to cancel a specific
  one, specify the job ID
```
sfdx force:source:deploy:cancel -i <jobid>
```
  Check the status of the cancel job
```
sfdx force:source:deploy:report
```

<a id="force-source-deploy-report" />

### `force:source:deploy:report`

###### USAGE
```
sfdx force:source:deploy:report [-w <minutes>] [-i <id>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -i, --jobid=jobid\
      job ID of the deployment you want to check; defaults to your most recent CLI deployment if not specified

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes 33

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Specify the job ID for the deploy you want to check. You can also specify a wait time (minutes) to check for updates to the deploy status.

  Examples:
  
  Deploy a directory of files to the org
```
sfdx force:source:deploy -d <directory>
```
  Now cancel this deployment and wait two minutes
```
sfdx force:source:deploy:cancel -w 2
```

  If you have multiple deployments in progress and want to cancel a specific one, specify the job ID
```
sfdx force:source:deploy:cancel -i <jobid>
```
  Check the status of the cancel job
```
sfdx force:source:deploy:report
```

<a id="force-source-open" />

### `force:source:open`

###### USAGE
```
sfdx force:source:open -f <filepath> [-r] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --sourcefile=sourcefile\
      (required) file to edit

  + -r, --urlonly\
      generate a navigation URL; don’t launch the editor

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command


###### DESCRIPTION
  NOTE: This command must be run from within a project.

  The file opens in your default browser.
  If no browser-based editor is available for the selected file, this command opens your org’s home page.
  To generate a URL for the browser-based editor but not open the editor, use --urlonly.

  Examples:
```
sfdx force:source:open -f Property_Record_Page.flexipage-meta.xml
sfdx force:source:open -f Property_Record_Page.flexipage-meta.xml -r
```

<a id="force-source-pull" />

### `force:source:pull`

###### USAGE
```
sfdx force:source:pull [-w <minutes>] [-f] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -f, --forceoverwrite\
      ignore conflict warnings and overwrite changes to the project

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes (default: 33)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  If the command detects a conflict, it displays the conflicts but does not complete the process. After reviewing the conflict, rerun the command with the --forceoverwrite parameter.

<a id="force-source-push" />

### `force:source:push`

###### USAGE
sfdx force:source:push [-f] [-g] [-w <minutes>] [-u <string>] [--apiversion <string>]

###### OPTIONS
  + -f, --forceoverwrite\
      ignore conflict warnings and overwrite changes to scratch org

  + -g, --ignorewarnings\
      deploy changes even if warnings are generated

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes (default: 33)

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  If the command detects a conflict, it displays the conflicts but does not complete the process. After reviewing the conflict, rerun the command with the --forceoverwrite parameter.

<a id="force-source-retrieve" />

### `force:source:retrieve`

###### USAGE
```
sfdx force:source:retrieve [-w <minutes>] [-x <filepath> | -m <array> | -p <array>] [-n <array>] [-u <string>] [-a <string>] [--verbose]
```

###### OPTIONS
  + -a, + --apiversion=apiversion\\
      target API version for the retrieve (default 46.0)

  + -m, --metadata=metadata\
      comma-separated list of metadata component names

  + -n, --packagenames=packagenames\
      a comma-separated list of packages to retrieve

  + -p, --sourcepath=sourcepath\
      comma-separated list of source file paths to retrieve

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -w, --wait=wait\
      [default: [object Object]] wait time for command to finish in minutes

  + -x, --manifest=manifest\
      file path for manifest (package.xml) of components to retrieve

  + --verbose\
      verbose output of retrieve result

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Use this command to retrieve source (metadata that’s in source format) from an org.
  To take advantage of change tracking with scratch orgs, use "```sfdx force:source:pull```".
  To retrieve metadata that’s in metadata format, use "```sfdx force:mdapi:retrieve```".

  The source you retrieve overwrites the corresponding source files in your local project. This command does not attempt to merge the source from your org with your local source files.

  If the comma-separated list you’re supplying contains spaces, enclose the entire comma-separated list in one set of double quotes.

  Examples:

  To retrieve the source files in a directory:
```
sfdx force:source:retrieve -p path/to/source
```
  To retrieve a specific Apex class and the objects whose source is in a directory:
```
sfdx force:source:retrieve -p path/to/apex/classes/MyClass.cls,path/to/source/objects
```
  To retrieve source files in a comma-separated list that contains spaces:
```
sfdx force:source:retrieve -p "path/to/objects/MyCustomObject/fields/MyField.field-meta.xml, path/to/apex/classes"
```
  To retrieve all Apex classes:
```
sfdx force:source:retrieve -m ApexClass
```
  To retrieve a specific Apex class:
```
sfdx force:source:retrieve -m ApexClass:MyApexClass
```
  To retrieve all custom objects and Apex classes:
```
sfdx force:source:retrieve -m CustomObject,ApexClass
```
  To retrieve all Apex classes and two specific profiles (one of which has a space in its name):
```
sfdx force:source:retrieve -m "ApexClass, Profile:My Profile, Profile: AnotherProfile"
```
  To retrieve all metadata components listed in a manifest:
```
sfdx force:source:retrieve -x path/to/package.xml
```

  To retrieve metadata from a package or multiple packages:
```
sfdx force:source:retrieve -n MyPackageName
sfdx force:source:retrieve -n "Package1, PackageName With Spaces, Package3"
```

  To retrieve all metadata from a package and specific components that aren’t in the package, specify both -n | --packagenames and one other scoping parameter:
  
```
sfdx force:source:retrieve -n MyPackageName -p path/to/apex/classes
sfdx force:source:retrieve -n MyPackageName -m ApexClass:MyApexClass
sfdx force:source:retrieve -n MyPackageName -x path/to/package.xml
```

<a id="force-source-status" />

### `force:source:status`

###### USAGE
```
sfdx force:source:status [-a] [-l] [-r] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --all\
      list all the changes that have been made

  + -l, --local\
      list the changes that have been made locally

  + -r, --remote\
      list the changes that have been made in the scratch org

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  NOTE: This command must be run from within a project.

  Examples:

```
sfdx force:source:status -l
sfdx force:source:status -r
sfdx force:source:status -a
sfdx force:source:status -a -u me@example.com --json
```

<a id="force-user-create" />

### `force:user:create`

###### USAGE
```
sfdx force:user:create [name=value...] [-f <filepath>] [-a <string>] [-v <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -a, --setalias=setalias\
      set an alias for the created username to reference within the CLI

  + -f, --definitionfile=definitionfile\
      file path to a user definition

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Create a user for a scratch org, optionally setting an alias for use by the
  CLI, assigning permission sets (e.g., permsets=ps1,ps2), generating a password (e.g., generatepassword=true), and setting User sObject fields.

  Examples:
```
sfdx force:user:create
sfdx force:user:create -a testuser1 -f config/project-user-def.json
sfdx force:user:create username=testuser1@my.org email=me@my.org permsets=DreamHouse
sfdx force:user:create -f config/project-user-def.json email=me@my.org generatepassword=true
```

<a id="force-user-display" />

### `force:user:display`

###### USAGE
```
sfdx force:user:display [-v <string>] [-u <string>] [--apiversion <string>]
```
 

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Output includes the profile name, org ID, access token, instance URL, login URL, and alias if applicable.
  Examples:

```
sfdx force:user:display
sfdx force:user:display -u me@my.org --json
```

<a id="force-user-list" />

### `force:user:list`

###### USAGE
```
sfdx force:user:list [-v <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  The original scratch org admin is marked with "(A)"
  
  Examples:
  
```
sfdx force:user:list
sfdx force:user:list -u me@my.org --json
sfdx force:user:list --json > tmp/MyUserList.json
```

<a id="force-user-password-generate" />

### `force:user:password:generate`

###### USAGE
```
sfdx force:user:password:generate [-o <array>] [-v <string>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -o, --onbehalfof=onbehalfof\
      comma-separated list of usernames for which to generate passwords

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + -v, --targetdevhubusername=targetdevhubusername\
      username or alias for the dev hub org; overrides default dev hub org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Generates and sets a random password for one or more scratch org users.
  If you haven’t set a default Dev Hub, or if your scratch org isn’t associated with your default Dev Hub, --targetdevhubusername is required.
  To see a password that was previously generated, run "```sfdx force:user:display```".

  Examples:

```
sfdx force:user:password:generate
sfdx force:user:password:generate -u me@my.org --json
sfdx force:user:password:generate -o user1@my.org,user2@my.org,user3@my.org
```

<a id="force-user-permset-assign" />

### `force:user:permset:assign`

###### USAGE
```
sfdx force:user:permset:assign -n <string> [-o <array>] [-u <string>] [--apiversion <string>]
```

###### OPTIONS
  + -n, --permsetname=permsetname\
      (required) the name of the permission set to assign

  + -o, --onbehalfof=onbehalfof\
      comma-separated list of usernames or aliases to assign the permission set to

  + -u, --targetusername=targetusername\
      username or alias for the target org; overrides default target org

  + --apiversion=apiversion\
      override the api version used for api requests made by this command

###### DESCRIPTION
  Defaults to the defaultusername.

  Examples:
  
```
sfdx force:user:permset:assign -n DreamHouse
sfdx force:user:permset:assign -n DreamHouse -u me@my.org
sfdx force:user:permset:assign -n DreamHouse -o user1@my.org,user2,user3
```

<a id="force-visualforce-component-create" />

### `force:visualforce:component:create`

###### USAGE
```
sfdx force:visualforce:component:create -n <string> -l <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      [default: 46.0] API version number

  + -d, --outputdir=outputdir\
      folder for saving the created files

  + -l, --label=label\
      (required) Visualforce component label

  + -n, --componentname=componentname\
      (required) name of the generated Visualforce component

  + -t, --template=DefaultVFComponent\
      [default: DefaultVFComponent] template to use for file creation



###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.
  Name and label are required.

  Examples:
  
```
sfdx force:visualforce:component:create -n mycomponent -l mylabel
sfdx force:visualforce:component:create -n mycomponent -l mylabel -d components
```

<a id="force-visualforce-page-create" />

### `force:visualforce:page:create`

###### USAGE

```
sfdx force:visualforce:page:create -n <string> -l <string> [-t <string>] [-d <string>] [-a <string>]
```

###### OPTIONS
  + -a, --apiversion=46.0|45.0\
      *[default: 46.0] API version number*
  + + -d, --outputdir=outputdir\\
      *folder for saving the created files*
  + -l, --label=label\
      *(required) Visualforce page label*
  + -n, --pagename=pagename\
      *(required) name of the generated Visualforce page*
  + -t, --template=DefaultVFPage\
      *[default: DefaultVFPage] template to use for file creation*

###### DESCRIPTION
  If not supplied, the apiversion, template, and outputdir use default values.
  The outputdir can be an absolute path or relative to the current working directory.
  Name and label are required.

  Examples:
```
sfdx force:visualforce:page:create -n mypage -l mylabel
sfdx force:visualforce:page:create -n mypage -l mylabel -d pages
```
<a id="plugins" />

### `plugins`

##### USAGE

```
sfdx plugins
```

##### OPTIONS
  + --core\
  *show core plugins*

##### EXAMPLE

```
sfdx plugins
```

COMMANDS
  plugins:generate   create a new sfdx-cli plugin
  plugins:install    installs a plugin into the CLI
  plugins:link       links a plugin into the CLI for development
  plugins:uninstall  removes a plugin from the CLI
  plugins:update     update installed plugins

TOPICS
  Run help for each topic below to view subcommands

  plugins:trust  pack an npm package and produce a tgz file along with a corresponding digital signature
  

<a id="plugins-generate" />

### `sfdx plugins:generate`

create a new sfdx-cli plugin

##### USAGE

```
sfdx plugins:generate [PATH]
```

##### OPTIONS
  --defaults  use defaults for every setting
  --force     overwrite existing files


<a id="plugins-install" />

### `sfdx plugins:install`

##### USAGE

```
sfdx plugins:install PLUGIN...
```

##### ARGUMENTS
  PLUGIN  plugin to install

##### OPTIONS
  + -f, --force\
  *yarn install with force flag*
  + -h, --help\
  *show CLI help*
  + -v, --verbose

##### DESCRIPTION
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command will override the core plugin implementation. This is useful if a user needs

  to update core plugin functionality in the CLI without the need to patch and update the whole CLI.

##### ALIASES

```
sfdx plugins:add
```

##### EXAMPLES

```
sfdx plugins:install myplugin
sfdx plugins:install https://github.com/someuser/someplugin
sfdx plugins:install someuser/someplugin
```

<a id="plugins-link" />

### `sfdx plugins:link`

##### USAGE

```
sfdx plugins:link PLUGIN
```

##### ARGUMENTS
  PATH  [default: .] path to plugin

##### OPTIONS
  + -h, --help\
  *show CLI help*
  + -v, --verbose

##### DESCRIPTION
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello' command will override the user-installed or core plugin implementation.
  This is useful for development work.

##### EXAMPLE

```
sfdx plugins:link myplugin
```

<a id="plugins-trust-sign" />

### `sfdx plugins:trust:sign`

pack an npm package and produce a tgz file along with a corresponding digital signature

##### USAGE

```
sfdx plugins:trust:sign -s <string> -p <string> -k <string> [--json] [--loglevel trace|debug|info|warn|error|fatal]
```

##### OPTIONS
  + -k, --privatekeypath=privatekeypath\
  *(required) the local file path for the private key.*
  + -p, --publickeyurl=publickeyurl\
  *(required) the url where the public key/certificate will be hosted.*
  + -s, --signatureurl=signatureurl\
  *(required) the url location where the signature will be hosted minus the name of the actual signature file.*
  

##### EXAMPLE

```
sfdx plugins:trust:sign --signature npmName-0.0.1.sig --publicKeyUrl https://developer.salesforce.com/media/salesforce-cli/sfdx.cer --privateKeyPath $HOME/secret.key
```

<a id="plugins-trust-verify" />

### `sfdx plugins:trust:verify`

##### USAGE

```
sfdx plugins:trust:verify -n <string> [-r <string>] [--json] [--loglevel trace|debug|info|warn|error|fatal]
```

##### OPTIONS
  + -n, --npm=npm\
  *(required) Specify the npm name. This can include a tag/version
  + -r, --registry=registry\
  *The registry name. the behavior is the same as npm.*  

##### EXAMPLES

```
sfdx plugins:trust:verifySignature --npm @scope/npmName --registry http://my.repo.org:4874
sfdx plugins:trust:verifySignature --npm @scope/npmName
```

<a id="plugins-uninstall" />

### `sfdx plugins:uninstall`

##### USAGE

```
sfdx plugins:uninstall PLUGIN...
```

##### ARGUMENTS
  PLUGIN  plugin to uninstall

##### OPTIONS
  + -h, --help\
  *show CLI help*
  + -v, --verbose

##### ALIASES

```
sfdx plugins:unlink
sfdx plugins:remove
```
