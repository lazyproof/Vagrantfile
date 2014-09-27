Vagrantfile
===========

- Runs CoreOS
- Opens a Port to your host computer
- Mounts shared folder

```sh
git clone https://github.com/lazyproof/Vagrantfile.git
cd Vagrantfile
./launch
```

Launch Script
```sh
vagrant up && vagrant ssh
sudo fig build
sudo fig up
#in another terminal window
sudo fig run web bundle exec rake db:create
sudo fig run web bundle exec rake db:migrate
#when you want to stop
sudo fig stop
```
