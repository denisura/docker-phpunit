docker-phpunit
==============

Run PHPUnit in Docker container

Build
--------------------

Build from `Dockerfile`:

    ``` sh
    sudo docker build  -t denisura/phpunit .
    ```

Verify build:

    ``` sh
    sudo docker run --rm -it denisura/phpunit --version
    ```

Usage
--------------------

1. Install the `denisura/phpunit` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/phpunit
    ```

2. Define an bash alias that runs this container whenever `phpunit` is invoked on the command line:

	``` sh
	$ echo "alias phpunit='docker run --rm -it -v \$(pwd):/workspace denisura/phpunit'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run phpunit as always:

	``` sh
	$ phpunit --version
	```