# WOSE
Web Oriented SQL Editor

WOSE is a development around the SQL Anywhere 16 / 17 database (by SAP/SYBASE) .
It's a way of creating WEB applications directly from the Sybase environment.
The whole development as well as all developent files are DB self-contained.

The SQLAnywhere 17 engine works as a full web-server. 
All tools are made available under classical web-browsers.

Using a simple web-bowser, WOSE provides :

- Editing capabilities of SQL, HTML, Javascript, CSS, Java via an ACE implementation

- A pre-compiler which resolves major features included in the WOSE specs

- Multi-developpers capability, with blocking functions at file or project level.

- Versionning system, with Version, Major, Minor and Build numbering system

    Versions are divided in :

      - Development version
      - Beta test version
      - Production version
      - Abandonned version

- Easy way to upgrade or downgrade a version for a file or a project

- The File system is divided in

Projects

      - Corresponds generally to an application, or part of it
      - groups a number of files of different types

Files
    
      - SQL tables, procedures, functions, views, services, events, triggers etc....
      - HTML
      - Javascript
      - CSS
      - Java
      - Images
      - etc...

Templating

    WOSE provides a number of usual templates permitting faster developments

      - models for HTML pages providing a basic structure based on a SQL table or view, including Javascript and CSS definitions
      - minimal models for creating functions, procedures, events, triggers, services from scratch
      - CSS models for white or dark global design pages
      - possibility to create new templates
      

SYSTEM CODING :

    ROOT sends incoming requests to the "apache' procedure which retrieves the data, formatted in consequence.
    
    The requests may be of type :
    
        HTML page

        JS document
        
        CSS document
        
        Image
        
        Video

    "HTML page" is principally formed in a function which name corresponds to the URL name and handles URL parameters as function's parameters
    
    The HTML "page - function" handles JS, Css, images, videos by requesting "apache" 
    
    The JS, CSS, images, videos are retrieved from the woseBlob table
