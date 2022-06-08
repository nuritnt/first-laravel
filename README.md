## Installation

If you cloned this project make sure to run the following steps:

1. `git clone project`
1. `cd project` 
1. ```
    docker run --rm \
        -u "$(id -u):$(id -g)" \
        -v $(pwd):/var/www/html \
        -w /var/www/html \
        laravelsail/php81-composer:latest \
        composer install --ignore-platform-reqs
    ```
1. In VS Code copy the file .env.example and renamed the copied file to .env (IMPORTANT: .env.example is still needed!) 
1. `./vendor/bin/sail`  // this command might change, check step serving the project
1. In the browser click on the button `generate key`
1. In the browser click on the link `refresh now`


## Serving the project

To start the server in development environment run the following command
`./vendor/bin/sail -f docker-compose-dev-sail.yml up`
