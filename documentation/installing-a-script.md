# Installing a script

Laravel Script sells Laravel scripts as source code. This page explains how to add a purchased script to a Laravel project and how to run it on your own machine or on a server. The steps below are a general outline. The exact commands and requirements for each script must be confirmed against that script's own files, so treat any step marked with a warning as something to check before you rely on it.

{% hint style="warning" %}
Needs verification: The exact installation steps for each script, including any Composer, npm or artisan commands. The product materials provided do not list them.
{% endhint %}

## Before you begin

Make sure you have the following ready:

- The script package you purchased from the Laravel Script website, downloaded to a location you can access.
- A working Laravel project, or a plan to create a new one. If you are not sure which to use, see the sections below.
- Access to a terminal and a code editor.
- The tools a Laravel application normally needs, such as PHP and Composer. Check the specific versions your script requires.

{% hint style="warning" %}
Needs verification: The server requirements for the scripts, including the required PHP version and extensions, the database engine, and the web server. Confirm these before you start.
{% endhint %}

Read the [License and usage terms](#) page before you install the script, so you know what you are permitted to do with the code.

## Option 1: Install into an existing Laravel project

Use this option if you already have a Laravel application and want to add the script's features to it.

1. **Back up your project.** Copy the project folder or commit your current changes to version control. This lets you return to the previous state if something goes wrong.
2. **Review the script's files.** Open the downloaded package and note which files and folders it contains, such as models, controllers, routes, views, migrations and configuration files.
3. **Copy the files into your project.** Place the script's files in the matching folders of your Laravel project. Do not overwrite your existing files unless the script instructions tell you to. If a file has the same name as one of yours, compare the two before you replace anything.
4. **Register routes and service providers, if required.** Some scripts ask you to add route definitions or register a provider in a configuration file. Follow the script's instructions exactly.
5. **Install dependencies.** If the script includes a dependency file, install the packages it lists.

{% hint style="warning" %}
Needs verification: Which dependency manager commands the script uses, and whether any front-end build step is needed.
{% endhint %}

6. **Configure the environment.** Copy the example environment file if the script provides one, then set the values it requires. Keep secret values out of version control.

{% hint style="warning" %}
Needs verification: The required environment variables and their expected values for each script.
{% endhint %}

7. **Run the database setup.** If the script includes migrations, run them to create the tables it needs.

{% hint style="warning" %}
Needs verification: Whether the script includes migrations or seed data, and the exact commands to run them.
{% endhint %}

## Option 2: Install into a new Laravel project

Use this option if you want a clean project that contains only the script.

1. **Create a new Laravel project** using the method recommended in the official Laravel documentation.
2. **Complete the basic setup** of the new project, including the environment file and the database connection.
3. **Copy the script's files** into the new project, following the same steps as Option 1.
4. **Install dependencies, configure the environment and run migrations** as described above.

{% hint style="info" %}
Tip: Test the new project with the default welcome page before you add the script. If it works, any problem that appears later is more likely to come from the script.
{% endhint %}

## Running the script locally

Once installation is complete, you can run the application on your own computer for testing.

1. Open a terminal in the project folder.
2. Start the development server with the Laravel command for local serving, or with the command the script documents.
3. Open the local address shown in the terminal in your web browser.
4. Check that the main pages load and that any forms or features work.

{% hint style="warning" %}
Needs verification: The local start command and the local address the script expects, and whether it needs a separate front-end process running at the same time.
{% endhint %}

{% hint style="info" %}
Tip: Keep debug mode on only while you test locally. Turn it off before you publish the site.
{% endhint %}

## Deploying to a server

To run the script on a live server:

1. Upload the project files to the server. Do not upload your local environment file, because it may contain passwords and keys. Create a new one on the server instead.
2. Point the web server's document root to the project's public folder.
3. Set the environment values for the production database and application URL.
4. Install dependencies in production mode, following the script's instructions.
5. Run the database migrations on the server.
6. Make sure the storage and cache folders are writable by the web server.
7. Visit the site and confirm that it works.

{% hint style="warning" %}
Needs verification: The exact production steps, the required folder permissions, and any scheduled tasks or queue workers the script needs.
{% endhint %}

## Demo data

{% hint style="warning" %}
Needs verification: Whether the script includes demo or seed data, and if so, how to load it and how to remove it before going live.
{% endhint %}

## Troubleshooting installation

If something goes wrong, check the following first:

- **A page shows an error after installation.** Check the application log and confirm the environment values are correct.
- **A database error appears.** Confirm the database connection settings and that the migrations have run.
- **A missing class or file error appears.** Confirm that all script files were copied to the correct folders and that dependencies are installed.

For more help, see the [Frequently asked questions and troubleshooting](#) page.
