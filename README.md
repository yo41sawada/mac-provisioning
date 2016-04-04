#Acknowledgment
this repository is based on mawatari.
https://github.com/mawatari/mac-provisioning

#Environment
##MacOS
10.11.4（El Capitan）


#Process
##バックアップ

* アカウント・Wifi情報
* 各種フォルダ
* FirefoxProfile
* iTunes w/ プレイリスト

##クリーンインストール
適宜
##再構築
###El Capitanで/usr/localが存在する場合
sudo chown $(whoami):admin /usr/local && sudo chown -R $(whoami):admin /usr/local

###Ansible実行環境

1. cd TARGET_DIR
1. ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
1. brew doctor
1. brew install python
1. brew install homebrew/versions/ansible18
1. brew install git
1. mkdir ~/.provisioning && cd $_
1. git clone https://github.com/yo41sawada/mac-provisioning.git .

###Ansible実行

1. HOMEBREW_CASK_OPTS="--appdir=/Applications" ansible-playbook -i hosts -vv yo41sawada_provisioning.yml

