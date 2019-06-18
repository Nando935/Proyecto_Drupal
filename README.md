
    Clone the last release
    Go to the project folder
    ddev start
    ddev composer install
    In the folder config/sync modify the file core.extension.yml change the profile: standard a profile: minimal and delete the     line standard: 1000
    If you have drush 9 ddev exec drush si --db-url=mysql://db:db@db/db --existing-config, or if you have drush 8 ddev exec drush si --db-url=mysql://db:db@db/db --config-dir=../config/sync
    In the folder web/sites/default modify the file settings.php, at the end below $config_directories['sync'] = '../config/sync', add $settings['default_content_deploy_content_directory'] = '../content';
    Import the configuration ddev exec drush cim -y
    Import the content default ddev exec drush dcdi
    Import the database ddev exec drush sqlc < fileDirectory

