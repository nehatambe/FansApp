# FansApp
Fans sharing encounter with their favorite celebrities 

Have you met a celebrity? If yes, go to our website ‘FanHub’, where you can post your experience with your favorite celebrity. The description along with an image can be posted on the website which will be visible to everyone. Description may contain user’s experience while his/her encounter with the celebrity. The user can also upload selfie or another related image he/she has captured with the celebrity. A user can like or dislike stories posted by other users. Also, information about any celebrity can be found through the website by navigating to the search a celebrity tab on the menu-bar. Another feature we have added to search celebrity is that the user can know more about the celebrity by clicking on “Read Info”. This redirects the user to IMDB website where the user can read more about the celebrity.

## Installation steps:
To Install browser-sync use following command 
``` 
npm install -g browser-sync
```
To install json-server use following command
 ```
npm install -g json-server
```
### Steps to launch an application:
The easiest way to get started is to clone repository
```
$ git clone https://github.com/devnigam24/FanPosts 
OR
Download the zip file from above repository and Unzip it.
```
Open another command prompt terminal and change to ‘FanPosts’ folder where you have the storiesdb.json file. To start json-server use following command.
```
json-server --port=3009 --watch storiesdb.json
```
After this command runs successful, open “http://localhost:3009/stories”
 
Open a new command prompt terminal and change directory where ‘FanPosts’ project is located(or where you have kept unzipped contents). To start browser-sync in server mode use following command 
```
browser-sync start --server --browser "Google Chrome" –files "stylesheets/*.css, scripts/*.js *.html"
```
(Note that although this website supports all major browsers, using this website in Google Chrome is recommended)
 
## Cloudinary Cloud Image Service 
To use your own cloud storage for storing images, you will need to create an account and obtain appropriate credentials: cloud_name, upload_preset 
More information about it can be found on the official website.

To update credentials, edit addClickHandler() function in js/formHandler.js. 
```
cloudinary.openUploadWidget({
                cloud_name: '<Cloud name which can be found on Dashboard of Cloudinary>',
                upload_preset: '<Generated Preset>',
                theme: 'minimal'
            }
```
