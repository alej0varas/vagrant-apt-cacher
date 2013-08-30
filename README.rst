=======================
 apt-cache for vagrant
=======================

Setup a apt-cacher server

  vagrant up
  vagrant ssh
  sudo apt-get update
  sudo apt-get install apt-cacher apache2 -y

Configure the server's Apt process to run through the cache

  In a terminal, type:

  sudo nano /etc/apt/apt.conf.d/01proxy

  Inside your new file, add a line that says:

  Acquire::http::Proxy "http://127.0.0.1:3142";

Client
======

  sudo nano /etc/apt/apt.conf.d/01proxy

  Inside your new file, add a line that says:

  Acquire::http::Proxy "http://10.0.2.2:3142";
