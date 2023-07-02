## Server Requirements

- PHP version `7.2` to `7.4` are supported, PHP version `≤5.6` and `8.0` are NOT supported. Please note that PHP needs to have the extensions `php-gd`, `php-bcmath`, `php-intl`, `php-openssl`, `php-mbstring` and `php-curl` installed and enabled.
- MySQL `5.5`, `5.6` and `5.7` are supported, also MariaDB replacement `10.x` is supported and might offer better performance.
- Apache `2.2` and `2.4` are supported. Nginx should work fine too, see [wiki page here](https://github.com/opensourcepos/opensourcepos/wiki/Local-Deployment-using-LEMP).
- Raspberry PI based installations proved to work, see [wiki page here](<https://github.com/opensourcepos/opensourcepos/wiki/Installing-on-Raspberry-PI---Orange-PI-(Headless-OSPOS)>).
- For Windows based installations please read [the wiki](https://github.com/opensourcepos/opensourcepos/wiki). There are closed issues about this subject, as this topic has been covered a lot.

## Local install

First of all, if you're seeing the message `system folder missing` after launching your browser, that most likely means you have cloned the repository and have not built the project.

1. Download the a [pre-release for a specific branch](https://github.com/opensourcepos/opensourcepos/packages/1047637) or the latest stable [from GitHub here](https://github.com/opensourcepos/opensourcepos/releases). A repository clone will not work unless know how to build the project.
2. Create/locate a new MySQL database to install Open Source Point of Sale into.
3. Execute the file `database/database.sql` to create the tables needed.
4. Unzip and upload Open Source Point of Sale files to the web-server.
5. Open `application/config/database.php` and modify credentials to connect to your database if needed.
6. Open `application/config/config.php` and swap the encryption key with your own.
7. Go to your install `public` dir via the browser.
8. Log in using
   - Username: admin
   - Password: pointofsale
9. Enjoy!
10. Oops, an issue? Please make sure you read the FAQ, wiki page, and you checked open and closed issues on GitHub. PHP `display_errors` is disabled by default. Create an` application/config/.env` file from the `.env.example` to enable it in a development environment.

## Local install using Docker

OSPOS can be deployed using Docker on Linux, Mac, and Windows. Locally or on a host (server).
This setup dramatically reduces the number of possible issues as all setup is now done in a Dockerfile.
Docker runs natively on Mac and Linux. Windows requires WSL2 to be installed. Please refer to the Docker documentation for instructions on how to set it up on your platform.

**