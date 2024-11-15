# Flysystem adapter for Infomaniak kDrive

[![Latest Version on Packagist][icon-version]][link-packagist]
[![Software License][icon-license]](LICENSE.md)
[![Total Downloads][icon-downloads]][link-packagist]

This package contains a [Flysystem](https://flysystem.thephpleague.com/) adapter for [Infomaniak kDrive](https://www.infomaniak.com/en/kdrive/). It is built on top of the Flysystem [WebDAV adapter](https://github.com/thephpleague/flysystem-webdav).

## Installation
Via [Composer](https://getcomposer.org/)
```shell script
composer require maa-solutions/flysystem-kdrive
```

## Credentials
To be able to connect to your kDrive, you'll need the following information.

1. Your kDrive ID ([Find your kDrive ID](#find-your-kdrive-id))
2. Your login email address (the one you'd use on https://manager.infomaniak.com)
3. A unique application password ([Generate an application password](https://manager.infomaniak.com/v3/profile/application-password))

### Find your kDrive ID
1. Connect to your kDrive directly on Infomaniak
2. Find your drive's ID in the URL : `https://drive.infomaniak.com/app/drive/[ID]/files`

## Usage

```php
use MaaSolutions\KDrive\KDriveAdapter;
use League\Flysystem\Filesystem;

$kDrive = new KDriveAdapter(
    '123456',               // Your kDrive's ID    
    'john.doe@example.tld', // Your Infomaniak login email address
    '********************', // Your generated password  
);

$filesystem = new Filesystem($kDrive);
```

## Examples
Go to the [examples](examples) directory to find a few examples to get you started.

## License
The MIT License (MIT). Please see the [LICENSE](LICENSE.md) for more information.

[icon-version]: https://img.shields.io/packagist/v/maa-solutions/flysystem-kdrive?style=flat-square
[icon-license]: https://img.shields.io/packagist/l/maa-solutions/flysystem-kdrive?style=flat-square
[icon-downloads]: https://img.shields.io/packagist/dt/maa-solutions/flysystem-kdrive?style=flat-square
[link-packagist]: https://packagist.org/packages/maa-solutions/flysystem-kdrive
