リポジトリの作成
================

マスターリポジトリの作成
------------------------

::

  $ sudo mkdir /var/hg/  # なければ作成
  $ sudo chown www:dev /var/hg/
  $ sudo su - www  # ユーザはdevグループの誰か
  $ mkdir /var/hg/example-prj/
  $ cd /var/hg/example-prj/
  $ hg init

作業リポジトリの作成
--------------------

::

  cd ~
  hg clone /var/hg/example-prj 

リリースリポジトリの作成
------------------------

::

  sudo su - www
  cd /var/hg/
  hg clone example-prj example-prj-release
