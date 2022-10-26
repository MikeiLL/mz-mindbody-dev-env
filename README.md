# WP_Env based plugin dev environment

## Make use of [wp-env](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-env/)
Start (or rebuild): `wp-env start`

## Unit Tests
```
wp-env run phpunit phpunit -c "/var/www/html/phpunit.xml.dist"
```

For a specific suite:

```
wp-env run phpunit phpunit -c "/var/www/html/phpunit.xml.dist" --testsuite Main
```

## For serving dev container over SSL:

Using [Mkcert](https://github.com/FiloSottile/mkcert)
```
brew install mkcert
brew install nss
mkcert -install
mkcert -cert-file mzmbo.test.pem -key-file mzmbo.test.key.pem mzmbo.test *.mzmbo.test
```
source: https://github.com/WordPress/wordcamp.org/blob/055fd1a66f036da5211ba489dc80a65e3d3a8081/.docker/readme.md#initial-setup

## Admin Portal
url `http://mzmbo.test:8888/wp-admin`
login: admin|password
