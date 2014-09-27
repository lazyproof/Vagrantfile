Vagrantfile
===========

This is designed for people with OSX, but can easily be adapted.

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
vagrant up
sudo fig build
sudo fig up
#in another terminal window
sudo fig run web bundle exec rake db:create
sudo fig run web bundle exec rake db:migrate
#when you want to stop
sudo fig stop
```

Fig.yml
```yml
db:
  image: postgres
  ports:
    - "5432"
web:
  image: rails_app
  command: bundle exec rails s
  ports:
    - "3000:3000"
  links:
    - db
```
