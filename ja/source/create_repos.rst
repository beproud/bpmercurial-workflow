リポジトリの作成
================

マスターリポジトリの作成
------------------------

``www`` ユーザでマスターリポジトリを作ります。 ``dev`` グループのすべてのユーザに書き込み権限を与えておきます。

::

  $ sudo mkdir /var/hg/  # なければ作成
  $ sudo chown www:dev /var/hg/
  $ sudo su - www  # ユーザはdevグループの誰か
  $ mkdir /var/hg/example-prj/
  $ cd /var/hg/example-prj/
  $ hg init
  $ chmod -R g+w example-prj

作業リポジトリの作成
--------------------

作業リポジトリは、各ユーザがマスターリポジトリを clone してホームディレクトリに作成します。

::

  $ cd ~
  $ hg clone /var/hg/example-prj 

個々人がリポジトリの扱い方を把握しているなら、作業リポジトリはこの形に縛る必要はありません。

リリースリポジトリの作成
------------------------

リリース用リポジトリは ``www`` ユーザでマスターリポジトリを clone して作成します。

::

  $ sudo su - www
  $ cd /var/hg/
  $ hg clone example-prj example-prj-release

