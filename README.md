# weather_app
angular js

npm install bootstrap @angular/material@19 @angular/cdk@19 @angular/animations@19

-------------------------------------------------------------------------------------------------------------------
for cors and proxy issues:
add this file "proxy.conf.json"
add this code to file :
{
  "/api": {
    "target": "https://api.openweathermap.org",
    "secure": true,
    "changeOrigin": true,
    "pathRewrite": { "^/api": "" }
  }
}

NOTICE : FOR RUN PROJECT WITH THIS FILE , USE THIS COMMAND :
ng serve --proxy-config proxy.conf.json
________________________________________

edit angular.json :
"serve": {
  "builder": "@angular-devkit/build-angular:dev-server",
  "options": { "proxyConfig": "proxy.conf.json" },
  ...
}
