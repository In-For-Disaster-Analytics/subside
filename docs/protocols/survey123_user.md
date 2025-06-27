---
title: Survey123 Connect
---

# ArcGIS Survey123 Connect

Part of the REDI suite of services includes access to the ArcGIS portal and Survey123 data collection tools.  This page will walk you through the steps for getting set up to use Survey 123.

## Onboarding / Credentialing
RESI users need credentials in order to utilize the Survey123 tools. To obtain credentials, reach out to the system Administrator [Paul?].  In your email include your Name, email, and the project / PI associated with your request. You will receive an email back with the necessary onboarding information:
- Username
- Tempoary Password
- Connection url
- Custom generated url for Trusted Connection with ESRI cloud and local portal
- link for downloading the Desktop application

### Forgotten password
The automatic password recoery tool is not currently functioning.  If you lose your access credentials / password, please contact the Administrator for a reset.

## Accessing Surveys 
To access your organizations surveys, login to the portal url provided, and then navigate to the 'survey 123 app' accessed via the 9 dot grid next to your username in the upper right corner of the screen. 

The landing screen will show you all the surveys created by you and other members of your organization.  To create a new survey click the '+ New Survey' button.

There are 3 options available for creating a new survey: The 'Blank Survey' and 'Template Survey' options use a web interface while the 'Survey 123 Connect' option requires the installation of a Desktop Application.  

The web based survey editor provides a simple, intuitive user interface with drag and drop capabilities, however it is limited in some of its features and the ability for more complex operations like nested or conditional questions. Those functionalities are available vie the Survey123 Connect Desktop Application.

To use the Web template simply click the 'Get started' button.

## Survey123 Connect: Advanced Surveys
### Launching Survey123 Connect Application
Follow the following steps to launch, install and connect to your organization's portal.
1. Download the 64-bit Desktop Application from the [Microsoft Store](https://apps.microsoft.com/detail/9pmst5c0dlst?rtc=1&hl=en-us&gl=US) or the [ESRI site] (https://www.esri.com/en-us/arcgis/products/arcgis-survey123/downloads)
2. Install tha application
3. After launching, navigate to the options bar (3 horizontal lines) in the top right and select 'Settings' 
4. Click the "+ Add connection" button and enter the ArcGIS connection URL provided in your onboarding email
5. Wait while the utility establishes a connection to the server - this may take a few minutes.
6. Sign in using the credentials for the portal you just connected to. 


### Advanced Template 
- Click 'New Survey' button
- Give new survey a meaningful name
- Samples has a lot of precreated sample surveys that feature different features / functions.  Can use as tutorials and delete later
- Select and create survey

###cd Re     Options
- Form (preview view), with options on left.
    - XLSForm opens spreadsheet that is driving the form
    - Update syncs spreadsheet to preview (but doesn't save changes in excel!). (Save in excel also does this.)
    - Files opens to local file system
    - Tools (analyze survey, etc.)
    - Publish, syncs to the portal and creates series of links to share
- Details
    - Description field
- Options
    - Set user permissions, etc.
- Map
    - Set overview and zoom for overall map in survey (?does it do this for multiple?)
- Media, basically project folder
    - CSVs for options
- Linked Content
    - Have to be published at least once for feature to turn on
    - ex. linked maps
- Scripts
    - Custom javascript
- Schema
    - Displays Layers/Tables, fields, field properties 

## Modifying XLS spreadsheet
- [documentation](https://doc.arcgis.com/en/survey123/desktop/create-surveys/xlsformessentials.htm)


## Publish
- Use defaults
- Analyze survey.  will give info on issues in form (basically a debugger)
- Resolve issues and publish
- Check on cloud survey123: put cutom url into new browser window address bar 
    - Repeat login with the same credentials
    - if says 'timed out', click login again

## Review Forms online
- Browser windows with tiles for forms, most recent in top left
- Opens into overview of submissions
- Collaborate
    - Survey share links under 
    - Controls for who can see, submit, etc.
    - Options to create Shared Update Group for collaborative form development and administration 

## Notes
- forms ONLY live locally until published