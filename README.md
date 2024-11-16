# Laravel Development and API Guide

This document provides you with a collection of **Artisan** and **Composer** commands to help with **Laravel application development**, **API setup**, **queue management**, **testing**, and much more.

## Table of Contents

- [Creating a New Laravel Application](#creating-a-new-laravel-application)
- [Basic Artisan Commands](#basic-artisan-commands)
- [Commands Related to API Development](#commands-related-to-api-development)
- [Composer Commands](#composer-commands)

---

## Creating a New Laravel Application

To get started with Laravel, follow these steps:

### **Most used commands**

```bash
composer create-project --prefer-dist laravel/laravel my-laravel-app   # Create a new Laravel application
```

```bash
cd my-laravel-app                 # Change directory into the new Laravel app                                               
```

```bash
cp .env.example .env               # Copy example env to .env
```

```bash
php artisan key:generate           # Generate the application key                                          
```

#
### BASIC ARTISAN COMMANDS


```bash
php artisan list                   # List all available artisan commands
```

```bash
php artisan help [command]         # Display help for a specific command        
```
#
### Development Server
```bash
php artisan serve                   # Start Laravel's built-in development server                       
```

#
### Application Key

```bash
php artisan key:generate              # Generate a new application key                 
```
#
## **Database Migrations**

```bash
php artisan migrate                    # Run the database migrations
```
```bash
php artisan migrate:rollback           # Rollback the last database migration
```
```bash
php artisan migrate:reset               # Rollback all database migrations
```
```bash
php artisan migrate:refresh             # Rollback and re-run all migrations
```
```bash
php artisan migrate:fresh               # Drop all tables and re-run all migrations
```
```bash
php artisan migrate:status              # Show the status of each migration
```

#
## Database Seeding

```bash
php artisan db:seed                       # Seed the database with records
```
```bash
php artisan db:seed --class=[ClassName]   # Seed specific class
```


#
## Creating Files

```bash
php artisan make:model [ModelName]         # Create a new Eloquent model
```
```bash
php artisan make:controller [ControllerName] # Create a new controller
```
```bash
php artisan make:middleware [MiddlewareName] # Create a new middleware
```
```bash
php artisan make:migration [MigrationName]  # Create a new migration
```
```bash
php artisan make:seeder [SeederName]        # Create a new database seeder
```
```bash
php artisan make:factory [FactoryName]      # Create a new factory
```
```bash
php artisan make:command [CommandName]      # Create a new custom Artisan command
```
```bash
php artisan make:event [EventName]          # Create a new event class
```
```bash
php artisan make:listener [ListenerName]    # Create a new listener class
```
```bash
php artisan make:job [JobName]              # Create a new job
```
```bash
php artisan make:policy [PolicyName]        # Create a new policy
```
```bash
php artisan make:resource [ResourceName]    # Create a new API resource
```
```bash
php artisan make:rule [RuleName]            # Create a new validation rule
```

#
### Cache & Configuration

```bash
php artisan config:cache                    # Cache the application's configuration
php artisan cache:clear                     # Clear the application cache
php artisan route:cache                     # Cache the application routes
php artisan view:clear                      # Clear the compiled views
php artisan config:clear                    # Clear the cached configuration
php artisan optimize                        # Optimize the framework for better performance
```
#
#
# Application Install (Custom Command)
```bash
php artisan install:api                     # Install and set up API-related components (custom command)
```
#
#
# Routing

```bash
php artisan route:list                      # List all registered routes
```
```bash
php artisan route:clear                     # Clear the route cache
```
```bash
php artisan route:cache                     # Cache the routes
```

#
#
# Queue Management

```bash
php artisan queue:listen                    # Listen to the queue jobs
```
```bash
php artisan queue:work                      # Start processing jobs in the queue
```
```bash
php artisan queue:restart                   # Restart the queue worker
```
```bash
php artisan queue:failed                    # List all failed queue jobs
```
```bash
php artisan queue:retry [job ID]            # Retry a specific failed job
```
```bash
php artisan queue:flush                     # Delete all failed jobs
```
#
#
# Artisan Tinker (Interactive REPL)
```bash
php artisan tinker                          # Launch the interactive REPL to interact with your application
```
#
#
# User Authentication (For versions < 6.x)
```bash
php artisan make:auth                       # Generate authentication scaffolding
```
#
#
# Storage & Logs
```bash
php artisan storage:link                    # Create a symbolic link from public/storage to storage/app/public
```
```bash
php artisan log:clear                       # Clear the log files
```
#
#
# Testing
```bash
php artisan test                            # Run the application tests using PHPUnit
```
#
#
# Other Commands

```bash
php artisan schedule:run                    # Run scheduled tasks (cron jobs)
```
```bash
php artisan vendor:publish                  # Publish package assets or configuration files
```
```bash
php artisan make:notification [NotificationName] # Create a new notification
```
#
#
--------------------------------------
# COMMANDS RELATED TO API DEVELOPMENT
--------------------------------------
#
#
# Set up API Authentication with Sanctum

```bash
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"  # Publish Sanctum's config
```
```bash
php artisan migrate                          # Run Sanctum migrations (for API authentication)
```
```bash
php artisan make:controller Api/[ControllerName] --api # Create an API controller (no create, edit methods)
```
```bash
php artisan make:model [ModelName]          # Create a new model (e.g., for API resources)
```
```bash
php artisan make:resource [ResourceName]    # Create an API resource for transforming models into JSON
```
```bash
php artisan make:middleware [MiddlewareName] # Create a middleware for API-related logic (e.g., auth, rate-limiting)
```
```bash
php artisan make:request [RequestName]      # Create a custom request class (for API validation)
```
```bash
php artisan make:seeder [SeederName]        # Create a seeder to populate API-related tables
```


# Testing API Routes

```bash
php artisan route:list                      # List all registered routes (including API routes)
```
```bash
php artisan route:cache                     # Cache the application API routes for better performance
```
```bash
php artisan route:clear                     # Clear cached routes
```
#
#

 -----------------------------
# COMPOSER COMMANDS
 -----------------------------

# Basic Commands

```bash
composer install                            # Install dependencies listed in composer.json
```
```bash
composer update                             # Update dependencies to their latest versions
```
```bash
composer require [package-name]             # Add a new package as a dependency
```
```bash
composer remove [package-name]              # Remove a package from the project
```
```bash
composer dump-autoload                      # Regenerate the Composer autoloader
```
```bash
composer create-project [vendor/package] [directory] # Create a new project from an existing package
```

#
#
# Dependency Management

```bash
composer show [package-name]                # Display details about a specific package
```
```bash
composer outdated                            # Check for outdated dependencies
```

# Autoloading

```bash
composer dump-autoload                      # Regenerate the autoloader files
```
```bash
composer dump-autoload --optimize           # Optimize the autoloader for production
```

#
#
# Updating Composer


```bash
composer self-update                        # Update Composer to the latest version
```
```bash
composer global update                      # Update globally installed Composer packages
```


# Composer Scripts

```bash
composer run-script [script-name]           # Run a custom script defined in composer.json
```
```bash
composer scripts                            # List all available Composer scripts
```


# Optimization

```bash
composer install --optimize-autoloader     # Optimize the autoloader during install (for production)
```
```bash
composer install --no-dev                   # Install dependencies without development dependencies (for production)
```
```bash
composer update --no-dev                    # Update dependencies without development dependencies
```


# Package Configuration

```bash
composer config [key] [value]               # Set a configuration value for Composer
```
```bash
composer config --global [key] [value]      # Set a global configuration value
```



# Composer Diagnostics

```bash
composer diagnose                           # Run checks to diagnose potential issues with Composer's configuration
```

