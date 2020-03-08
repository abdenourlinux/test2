# Bash Script: magento-backup-rollback
This utility help you backup and restore Magento2 files and database.

## Getting Started
These instructions will get you a copy of the tools up and running on your local machine for development and testing purposes. 
See deployment for notes on how to deploy the tools on a live system.

### Prerequisites
For the scripts to work properly, the n98-magerun2 CLI tool for Magento2 needs to be installed on the system: 
``` 
wget https://files.magerun.net/n98-magerun2.phar
chmod +x n98-magerun2.phar
sudo mv n98-magerun2.phar /usr/local/bin/
```

You can test this is installed correctly using the following command:

``` n98-magerun2.phar list```

### Installation
To install the utility on your system you need simply to downoad it from this git repository:

``` git clone https://github.com/quantiota/magento-backup-rollback ```

## Usage:
### Default Variables:
Some default values are defined on the utility such as `backup location` and Magento `DocumentRoot`, Please change those variable according to your setup.

`MAGENTO_ROOT` default value is  `/var/www/html/magento`

`BACKUP_PATH` default value is `/var/www/html/magento/var/backups`

### Options
The `backup.sh` script doean not accept any options.

The `rollback.sh` script accepts two options:

    -f : To specify the archived files version to be retrored.
    
    -d : To specify the archived database version to be restored.
## Examples
### To backup files and database into default location:

`sudo bash  backup.sh`

### To restore a file:
`sudo bash rallback.sh -f /path/to/archive.tar.gz`

### To restore a database file:
`sudo bash rallback.sh -d /path/to/archive.sql`







