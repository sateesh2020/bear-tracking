# Ursus Park sample app for Trailhead project Build Flexible Apps with Lightning Web Components

### Requirements
* A Salesforce Developer Account / Trailhead Playground ( https://www.salesforce.com/form/signup/prerelease-spring19/ )
* SFDX CLI ( https://developer.salesforce.com/tools/sfdxcli)

Follow this trailhead to setup SFDX CLI  (https://trailhead.salesforce.com/en/content/learn/modules/sfdx_app_dev/sfdx_app_dev_setup_dx)

### Set Up the Ursus Park App

Open a command prompt, such as cmd on Windows or Terminal on MacOS.
Clone the Ursus Park app git repository.
```sh
  git clone  https://github.com/sateesh2020/bear-tracking.git
```
The repository contains the Ursus Park app, a Bear object with a set of fields, record and page layouts, and Apex code that retrieves bear records and sample bear records. This project base helps us focus on the Lightning Web Component development.

Navigate to the new build-apps-with-lwc directory.
```sh
  cd bear-tracking
```
Authorize your Trailhead Playground with the Salesforce CLI, save it with a bear-tracking alias and set the current user as the default user:
```sh
  sfdx force:auth:web:login -s -a bear-tracking
```
When a browser window with the Salesforce login page opens, enter your Trailhead Playground credentials.
Deploy the app code to the org.
```sh
sfdx force:source:deploy -p force-app/main/default
```
Assign the Ursus Park User permission set to the current user.
```sh
sfdx force:user:permset:assign -n Ursus_Park_User
```
Import the sample data.
```sh
sfdx force:data:tree:import -p data/plan.json
```
Open the org in a browser.
```sh
sfdx force:org:open
```



