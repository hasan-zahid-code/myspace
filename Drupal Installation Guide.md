# Drupal Installation Guide

This guide provides instructions to set up a new Drupal instance with essential modules. Follow the steps below to install and enable the specified modules.

## Prerequisites

- Ensure you have Composer installed on your system.
- Ensure you have Drush installed on your system.

## Step 1: Create a New Drupal Project

First, create a new Drupal project using Composer:

```sh
composer create-project drupal/recommended-project my_site_name
cd my_site_name


## Step 2: Install Required Modules

```sh
composer require -W drupal/cors_ui:^1.0
composer require -W drupal/jsonapi:^3.0
composer require -W drupal/jsonapi_menu_items:^2.0
composer require -W drupal/token:^1.10
composer require -W drupal/key:^2.0
composer require -W drupal/jwt:^1.0
composer require -W drupal/rest_menu_items:^1.0
composer require -W drupal/restui:^1.22
composer require -W drupal/svg_image:^2.0
composer require -W drupal/svg_image_responsive:^1.0
composer require -W drupal/svg_formatter:^1.0
composer require -W drupal/openapi:^2.0
composer require -W drupal/openapi_ui:^1.0
composer require -W drupal/swagger_ui:^1.0


## Step 3: Enable Installed Modules

```sh
drush en cors_ui -y
drush en jsonapi -y
drush en jsonapi_menu_items -y
drush en token -y
drush en key -y
drush en jwt -y
drush en rest_menu_items -y
drush en restui -y
drush en svg_image -y
drush en svg_image_responsive -y
drush en svg_formatter -y
drush en openapi -y
drush en openapi_ui -y
drush en swagger_ui -y


## Step 4: Rebuild Cache

```sh
drush cr


## Uninstalling Modules

### Remove Module with Composer

composer remove drupal/MODULENAME

### Uninstall Module with Drush

drush pm-uninstall MODULENAME -y

