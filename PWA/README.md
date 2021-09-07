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
 
 [
  '/**',           // Include all URLs.
  '!/**/*.*',      // Exclude URLs to files.
  '!/**/*__*',     // Exclude URLs containing `__` in the last segment.
  '!/**/*__*/**',  // Exclude URLs containing `__` in any other segment.
]


 "dataGroups": [
        {
      "name": "blog",
      "urls": ["https://citywoofer.com/blog/**"],
      "cacheConfig": {
        "strategy": "freshness",
        "maxSize": 100,
        "maxAge": "0d",
        "timeout": "1s"
      }
    },
    {
      "name": "blogs_",
      "urls": ["https://www.citywoofer.com/blog"],
      "cacheConfig": {
        "strategy": "freshness",
        "maxSize": 100,
        "maxAge": "0d",
        "timeout": "1s"
      }
    },
    {
      "name": "blog_",
      "urls": ["https://citywoofer.com/blog"],
      "cacheConfig": {
        "strategy": "freshness",
        "maxSize": 100,
        "maxAge": "0d",
        "timeout": "1s"
      }
    }
  ]
