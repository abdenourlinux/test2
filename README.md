# Bash Script: magento-backup-rollback
This utility helps you backup and restore Magento2 files and databases.

## Getting Started
These instructions will get you a copy of the tools up and running on your local machine for development and testing purposes. 

### Prerequisites
For the utility to work properly, the n98-magerun2 CLI tool for Magento2 needs to be installed on the system, you can download it from this link: 

`  https://files.magerun.net/n98-magerun2.phar `

### Installation
To install the utility on your system you need to download (clone) it from this git repository:

```
git clone https://github.com/quantiota/magento-backup-rollback 
cd magento-backup-rollback
chmod +x backup.sh rollback.sh
```

## Usage:
### Default Variables:
Some default values are defined on the utility such as `backup location` and Magento `DocumentRoot`, Please change those variable according to your setup.

`MAGENTO_ROOT` default value is  `/var/www/html/magento`

`BACKUP_PATH` default value is `/var/www/html/magento/var/backups`

### Options
The `backup.sh` script does not accept any options.

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







