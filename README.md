# cloud-foundry-local-installation-macbook-pro
### pre-req:
1. install vagrant from vagrantup.com
2. install brew ```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
3. install brew cask ```brew install caskroom/cask/brew-cask```
4. install virtual box ``` brew cask install virtualbox```
5. install spiff
 
```bash
 brew tap xoebus/homebrew-cloudfoundry
 brew install spiff
```
 
### install
```bash
sudo gem install bosh_cli
mkdir cloudfoundry
cd cloudfoundry
git clone https://github.com/cloudfoundry/bosh-lite
cd bosh-lite
vagrant up --provider=virtualbox
bosh target 192.168.50.4 lite
bosh login
bin/add-route
cd ..
git clone https://github.com/cloudfoundry/cf-release
cd cf-release
./update
cd ../bosh-lite/
./bin/provision_cf
```
