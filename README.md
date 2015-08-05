# cloud-foundry-local-installation-macbook-pro
### pre-req:
1. install vagrant from vagrantup.com

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
```
