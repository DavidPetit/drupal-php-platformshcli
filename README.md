# Dokcer image wodby/drupal-php with Platform.sh CLI included

A version of wodby/drupal-php image with Platform.sh CLI included

You can run platform.sh cli from the container based on this image. To use you platform,sh account, you only need to set a platform.sh API token: https://docs.platform.sh/gettingstarted/cli/api-tokens.html and set an environemnt variable named PLATFORMSH_CLI_TOKEN with your token to be used by your php container.

For example, using docker-compose, you can have something like this at the begining of the configuration for php container:
```
php:
    build: petitdavid/drupal-php-platformshcli:$PHP_TAG
    container_name: "${PROJECT_NAME}_php"
    environment:
      PLATFORMSH_CLI_TOKEN: ${PLATFORMSH_CLI_TOKEN}
```
