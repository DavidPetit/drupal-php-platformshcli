# Docker image wodby/drupal-php with Platform.sh CLI

[DavidPetit/drupal-php-platformshcli](https://hub.docker.com/r/petitdavid/drupal-php-platformshcli) is a version of [wodby/drupal-php](https://github.com/wodby/drupal-php) image with Platform.sh CLI included.

You can run platform.sh cli from the container based on this image and still inherit all the same goodness from [wodby/drupal-php](https://github.com/wodby/drupal-php).

To connect the cli to your platform.sh account, you only need to create a platform.sh API token: https://docs.platform.sh/gettingstarted/cli/api-tokens.html and set an environemnt variable named PLATFORMSH_CLI_TOKEN with your token in order to be used by your php container.

For example, using docker-compose and from arguments from a .env file, you can have something like this at the begining of the configuration for php container:
```
php:
    image: petitdavid/drupal-php-platformshcli:$PHP_TAG
    container_name: "${PROJECT_NAME}_php"
    environment:
      PLATFORMSH_CLI_TOKEN: ${PLATFORMSH_CLI_TOKEN}
```

Supported tags and respective `Dockerfile` links:

* `7.3`  [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/master/php-7.3/Dockerfile)
* `7.2` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/master/php-7.2/Dockerfile)
* `7.1` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/dev/php-7.1/Dockerfile)
* `7.3-dev` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/dev/php-7.3/Dockerfile)
* `7.2-dev` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/dev/php-7.2/Dockerfile)
* `7.1-dev` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/dev/php-7.1/Dockerfile)
* `7.3-dev-macos` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/macos/php-7.3/Dockerfile)
* `7.2-dev-macos` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/macos/php-7.2/Dockerfile)
* `7.1-dev-macos` [_Dockerfile_](https://github.com/DavidPetit/drupal-php-platformshcli/tree/macos/php-7.1/Dockerfile)
