# PWA

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 11.1.4.

# Step create PWA
1. ng add @angular/pwa
2. npm i -g http-server
3. How to run pwa
### Long process to run PWA application

    i. Run ng build --prod command. It will create files under dist/ folder.
    ii. cd dist/, cd project-name, npx http-server

   ### Short process to run PWA application
       
       i.  Add in package.json       
        "start-pwa": "ng build --prod && http-server -p 8080 -c-1 dist/PWA"        
    NOTE: Make sure dist/your-project-name  project name, uppercase, lowercase should be same   
    
       ii. Run
        npm run start-pwa

For test ->
1. in network tab make offline and refresh page
2. in application tab Service Workers
    source ngsw-worker.js

 Study in detail -> https://angular.io/guide/service-worker-config
    Reference ->     https://medium.com/ngconf/angular-pwa-install-and-configure-858dd8e9fb07
