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

  echo 'Acquire::http::Proxy "http://127.0.0.1:3142";' | sudo tee /etc/apt/apt.conf.d/01proxy

Client
======

  In a terminal, type:

  echo 'Acquire::http::Proxy "http://10.0.2.2:3142";' | sudo tee /etc/apt/apt.conf.d/01proxy
