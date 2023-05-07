<div align="center">
    <a href="https://php.net">
        <img
            alt="PHP"
            src="https://www.php.net/images/logos/new-php-logo.svg"
            width="150">
    </a>
</div>

# The PHP Interpreter

PHP is a popular general-purpose scripting language that is especially suited to
web development. Fast, flexible and pragmatic, PHP powers everything from your
blog to the most popular websites in the world. PHP is distributed under the
[PHP License v3.01](LICENSE).


## Documentation

The PHP manual is available at [php.net/docs](https://php.net/docs).

## Installation

### Prebuilt packages and binaries

Prebuilt packages and binaries can be used to get up and running fast with PHP.

For Windows, the PHP binaries can be obtained from
[windows.php.net](https://windows.php.net). After extracting the archive the
`*.exe` files are ready to use.

For other systems, see the [installation chapter](https://php.net/install).

### Building PHP source code



For a minimal PHP build from Git, you will need autoconf, bison, and re2c. For
a default build, you will additionally need libxml2 and libsqlite3.

On Ubuntu, you can install these using:

    sudo apt install -y pkg-config build-essential autoconf automake libtool bison re2c \
                        libxml2-dev libsqlite3-dev
                        

clone reposity in your ubuntu

    git clone https://github.com/php/php-src.git

change directory to php-src

    cd php-src

select php version 

    git checkout PHP-8.2

build configuration
    
    ./buildconf

configure with installation path and attach extensions like openssl , mbstring etc and enable-zts 

    ./configure --prefix=$HOME/myphpnew  -with-bcmath --with-curl --with-json --with-mbstring --with-mysql --with-tokenizer --with-xml --with-zip --enable-debug --enable-zts  --enable-mbstring --enable-bcmath --enable-mysqlnd --with-openssl --with-openssl-dir=$HOME/myphpnew/ssl --with-pear

make the code

    make -j

install the code

    make install

make this is a default php 

    cp $HOME/myphpnew/bin/* /usr/local/bin

install parallel extension

    pecl install parallel


check installed modules

    php -m 


    ************* THANK YOU *************