# -----------------------------
# CREATING A NEW LARAVEL APPLICATION
# -----------------------------
composer create-project --prefer-dist laravel/laravel my-laravel-app   # Create a new Laravel application
cd my-laravel-app                                                   # Change directory into the new Laravel app

# Copy the .env.example file to .env and generate the application key
cp .env.example .env                                               # Copy example env to .env
php artisan key:generate                                            # Generate the application key

# -----------------------------
# BASIC ARTISAN COMMANDS
# -----------------------------
php artisan list                             # List all available artisan commands
php artisan help [command]                   # Display help for a specific command

# Development Server
php artisan serve                            # Start Laravel's built-in development server

# Application Key
php artisan key:generate                     # Generate a new application key

# Database Migrations
php artisan migrate                         # Run the database migrations
php artisan migrate:rollback                # Rollback the last database migration
php artisan migrate:reset                   # Rollback all database migrations
php artisan migrate:refresh                 # Rollback and re-run all migrations
php artisan migrate:fresh                   # Drop all tables and re-run all migrations
php artisan migrate:status                  # Show the status of each migration

# Database Seeding
php artisan db:seed                         # Seed the database with records
php artisan db:seed --class=[ClassName]     # Seed specific class

# Creating Files
php artisan make:model [ModelName]          # Create a new Eloquent model
php artisan make:controller [ControllerName] # Create a new controller
php artisan make:middleware [MiddlewareName] # Create a new middleware
php artisan make:migration [MigrationName]  # Create a new migration
php artisan make:seeder [SeederName]        # Create a new database seeder
php artisan make:factory [FactoryName]      # Create a new factory
php artisan make:command [CommandName]      # Create a new custom Artisan command
php artisan make:event [EventName]          # Create a new event class
php artisan make:listener [ListenerName]    # Create a new listener class
php artisan make:job [JobName]              # Create a new job
php artisan make:policy [PolicyName]        # Create a new policy
php artisan make:resource [ResourceName]    # Create a new API resource
php artisan make:rule [RuleName]            # Create a new validation rule

# Cache & Configuration
php artisan config:cache                    # Cache the application's configuration
php artisan cache:clear                     # Clear the application cache
php artisan route:cache                     # Cache the application routes
php artisan view:clear                      # Clear the compiled views
php artisan config:clear                    # Clear the cached configuration
php artisan optimize                        # Optimize the framework for better performance

# Application Install (Custom Command)
php artisan install:api                     # Install and set up API-related components (custom command)

# Routing
php artisan route:list                      # List all registered routes
php artisan route:clear                     # Clear the route cache
php artisan route:cache                     # Cache the routes

# Queue Management
php artisan queue:listen                    # Listen to the queue jobs
php artisan queue:work                      # Start processing jobs in the queue
php artisan queue:restart                   # Restart the queue worker
php artisan queue:failed                    # List all failed queue jobs
php artisan queue:retry [job ID]            # Retry a specific failed job
php artisan queue:flush                     # Delete all failed jobs

# Artisan Tinker (Interactive REPL)
php artisan tinker                          # Launch the interactive REPL to interact with your application

# User Authentication (For versions < 6.x)
php artisan make:auth                       # Generate authentication scaffolding

# Storage & Logs
php artisan storage:link                    # Create a symbolic link from public/storage to storage/app/public
php artisan log:clear                       # Clear the log files

# Testing
php artisan test                            # Run the application tests using PHPUnit

# Other Commands
php artisan schedule:run                    # Run scheduled tasks (cron jobs)
php artisan vendor:publish                  # Publish package assets or configuration files
php artisan make:notification [NotificationName] # Create a new notification

# -----------------------------
# COMMANDS RELATED TO API DEVELOPMENT
# -----------------------------

# Set up API Authentication with Sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"  # Publish Sanctum's config
php artisan migrate                          # Run Sanctum migrations (for API authentication)
php artisan make:controller Api/[ControllerName] --api # Create an API controller (no create, edit methods)
php artisan make:model [ModelName]          # Create a new model (e.g., for API resources)
php artisan make:resource [ResourceName]    # Create an API resource for transforming models into JSON
php artisan make:middleware [MiddlewareName] # Create a middleware for API-related logic (e.g., auth, rate-limiting)
php artisan make:request [RequestName]      # Create a custom request class (for API validation)
php artisan make:seeder [SeederName]        # Create a seeder to populate API-related tables

# Testing API Routes
php artisan route:list                      # List all registered routes (including API routes)
php artisan route:cache                     # Cache the application API routes for better performance
php artisan route:clear                     # Clear cached routes

# -----------------------------
# COMPOSER COMMANDS
# -----------------------------

# Basic Commands
composer install                            # Install dependencies listed in composer.json
composer update                             # Update dependencies to their latest versions
composer require [package-name]             # Add a new package as a dependency
composer remove [package-name]              # Remove a package from the project
composer dump-autoload                      # Regenerate the Composer autoloader
composer create-project [vendor/package] [directory] # Create a new project from an existing package

# Dependency Management
composer show                                # Display installed packages and their versions
composer show [package-name]                # Display details about a specific package
composer outdated                            # Check for outdated dependencies

# Autoloading
composer dump-autoload                      # Regenerate the autoloader files
composer dump-autoload --optimize           # Optimize the autoloader for production

# Updating Composer
composer self-update                        # Update Composer to the latest version
composer global update                      # Update globally installed Composer packages

# Composer Scripts
composer run-script [script-name]           # Run a custom script defined in composer.json
composer scripts                            # List all available Composer scripts

# Optimization
composer install --optimize-autoloader     # Optimize the autoloader during install (for production)
composer install --no-dev                   # Install dependencies without development dependencies (for production)
composer update --no-dev                    # Update dependencies without development dependencies

# Package Configuration
composer config [key] [value]               # Set a configuration value for Composer
composer config --global [key] [value]      # Set a global configuration value

# Composer Diagnostics
composer diagnose                           # Run checks to diagnose potential issues with Composer's configuration
