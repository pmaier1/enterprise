# ownCloud / enterprise

Download this repository to build ownCloud enterprise docker images

## Build ownCloud enterprise

Building ownCloud Enterprise with access to the Customer Portal
```bash
./build username
```
You will be asked for the Password next.


## Build your ownCloud enterprise image from tarball

1. Download ownCloud Enterprise ```owncloud-enterprise-complete-9.0.3.tar.bz2``` from ownCloud's Customer Download Center to this folder.
2. Replace the `curl` command for loading tarball from URL in Dockerfile with 

```
   ADD owncloud-enterprise-complete-9.0.3.tar.bz2 /var/www/
   RUN chown -R www-data.www-data /var/www/owncloud
```

3. Build and run your ownCloud Enterprise Dockerfile

```
docker build -t owncloud/enterprise:9.0.3 .
```

Now you can use the image `owncloud/enterprise` exactly like `owncloud/server`
Further instructions see [owncloud/server](https://github.com/owncloud-docker/server)


## Versions

Versions can be found as branches of this repository

* [latest](https://github.com/owncloud-docker/enterprise/tree/master) download [zip](https://github.com/owncloud-docker/enterprise/archive/master.zip)
* [9.0.3](https://github.com/owncloud-docker/enterprise/tree/9.0.3) download [zip](https://github.com/owncloud-docker/enterprise/archive/9.0.3.zip)

