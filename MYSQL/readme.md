### If you had had previouosly installed mysql and then deleted this is how you reset root password
https://stackoverflow.com/questions/9695362/macosx-homebrew-mysql-root-password
$ brew services stop mysql
$ pkill mysqld
$ rm -rf /usr/local/var/mysql/ # NOTE: this will delete your existing database!!!
$ brew postinstall mysql
$ brew services restart mysql
$ mysql -uroot