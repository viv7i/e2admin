E2 Admin Project Template
===============================

E2 Admin Project Template is a skeleton base application for
starting admin development in Yii2 web framework.

The template includes three tiers: front end, back end, and console, each of which
is a separate Yii application.

The template uses AdminLTE as a html template.

The project contains following modules to get started - 

<ul>
<li>Dashboard</li>
<li>Users</li>
<li>Access Control</li>
<li>CMS Manager</li>
<li>Email Manager</li>
<li>Settings</li>
</ul>

It also features two themes alongwith default theme comes with yii2 framework and language swither in frontend.

DIRECTORY STRUCTURE
-------------------

```
common
    components/             contains helper modules that boostraped with application
    config/             contains shared configurations
    mail/                contains view files for e-mails
    messages/               contains messages translations files for i18n 
    models/              contains model classes used in both backend and frontend
    tests/               contains tests for common classes
    widgets/            contains common widgets
console
    config/              contains console configurations
    controllers/         contains console controllers (commands)
    migrations/          contains database migrations
    models/              contains console-specific model classes
    runtime/             contains files generated during runtime
backend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains backend configurations
    controllers/         contains Web controller classes
    models/              contains backend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for backend application    
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
frontend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains frontend configurations
    controllers/         contains Web controller classes
    models/              contains frontend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for frontend application
    themes/             contains template theme view files            
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
    widgets/             contains frontend widgets
vendor/                  contains dependent 3rd-party packages
environments/            contains environment-based overrides
```

REQUIREMENTS
----------------------

The minimum requirement by this project template is that your Web server supports PHP 5.4.0.

INSTALLATION
--------------------

To intalll web framework run following commands in terminal -
<pre>
    <code>
        composer global require "fxp/composer-asset-plugin:^1.2.0"
        composer create-project --prefer-dist yiisoft/yii2-app-advanced yii-application
    </code>
</pre>

PREPARING APPLICATION
-----------------------------------
<ol>
<li><p>Open a console terminal, execute the <code>init</code> command and select <code>dev</code> as environment.</p>

<pre><code>
    /path/to/php-bin/php /path/to/yii-application/init
</code></pre>

<p>If you automate it with a script you can execute <code>init</code> in non-interactive mode.</p>

<pre><code>
    /path/to/php-bin/php /path/to/yii-application/init --env=Development --overwrite=All
</code></pre>

</li>
<li><p>Create a new database and adjust the <code>components['db']</code> configuration in <code>common/config/main-local.php</code> accordingly.</p></li>
<li><p>Open a console terminal and pull the repository then  apply migrations with command <code>/path/to/php-bin/php /path/to/yii-application/php yii migrate</code>.</p></li>
<li><p>Now  enable access controls with this migration command <code>/path/to/php-bin/php /path/to/yii-application/php yii migrate --migrationPath=@yii/rbac/migrations
</code>.</p></li>
<li><p>And update dependencies with command <code>/path/to/php-bin/php /path/to/yii-application/composer update</code>.</p></li>
</ol>

CONFIGURATION
-----------------------------------

The project uses following third party modules to enhance the user experience.

<ul>
<li><a href="https://github.com/wbraganca/yii2-dynamicform">yii2-dynamicform</a><p>To use add this line to composer.json file's require section </p><code>"wbraganca/yii2-dynamicform": "*"</code></li>
<li><a href="https://github.com/yiidoc/yii2-redactor">yii2-redactor</a><p>To use add this line to composer.json file's require section </p><code> "yiidoc/yii2-redactor": "*"</code></li>
<li><a href="https://github.com/kartik-v/yii2-widget-datepicker">yii2-widget-datepicker</a><p>To use add this line to composer.json file's require section </p><code>"kartik-v/yii2-widget-datepicker": "@dev"</code></li>
</ul>
