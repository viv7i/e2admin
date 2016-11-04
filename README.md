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

The minimum requirement by this project template is Apache Web server that supports PHP 5.4.0.

INSTALLATION
--------------------

clone this repository using following command -
<pre>
    <code>
        git clone [repository name]
    </code>
</pre>

PREPARING APPLICATION
-----------------------------------
<ol>
<li><p>Once project has been cloned open terminal and move to your project folder path.<p>
<p>Run <code>composer install</code> command to install all framework requirement</p>
</li>
<li><p>Create a new database and adjust the <code>components['db']</code> configuration in <code>common/config/main-local.php</code> accordingly.</p></li>
<li><p>Now apply migrations with command <code>php yii migrate</code>.</p></li>
<li><p>To enable access controls run this migration command <code>php yii migrate --migrationPath=@yii/rbac/migrations</code> followed by <code>php yii rbac/init</code> command.</p></li>
</ol>
