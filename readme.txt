WebPress is an open source PHP library of core functionality for web applications.
It includes the foundations you need to build robust, scalable web applications.

TODO

**INSTALL SCRIPT**
If no wp-config.php exists,
redirect to install page where it starts the installation script.

Users will be able to set all their application settings along
with selecting WebPress APIs needed in their app.

If the user needs a database, the install script will allow the user
to create their schema visually. The script then creates a new wp-schema.php.

FR (Feature Request): Install script could setup basic routes for the app too in wp-app?

WebPress Features:
# Add the following features to your WebPress Application:
- Database connections
- Taxonomies (requires DB)
- Options management (requires DB)

- Users (requires DB)
- Admin (requires Users, DB)

Additional Features:
- Content Publishing (requires DB)

Low Level APIs:
- Logging
- XML-RPC Server and Client
- Object caching
- Router/Dispatcher

Core APIs:
- XSS and SQL injection protection (including a variety of powerful escaping functions)

Directory Structure:

WebPress: LOAD STACK
=====================
A request to the application (i.e. http://example.com).

.htaccess (optional for pretty urls)
index.php // Front controller loads the WebPress enviroment.
-	wp-load.php	// finds and loads wp-config.php and wp-settings.php, else triggers install script.
	-	wp-config.php // global configuration file stores all application settings.
	-	wp-settings.php // Loads all the needed WebPress libraries and does the preliminary work. Includes the application's index.php if the router is enabled.
		-	WebPress/*
		-	wp-plugins/*
		-	wp-app/*

GOALS:

Future Stuff:
- Admin scafolding based on db
- db crud

- PHP5 OOP