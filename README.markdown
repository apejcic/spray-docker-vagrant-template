## _spray-docker-vagrant_ Template Project

This template provides a starting point for running _[Spray](http://spray.io/)_ projects or any other _Scala_ powered project within _Docker_ container.

It's just a start, but you immediately get:

- Server running inside docker is accessible via 8080 port on the host machine.
- Live code reloading.
- Portable environment.
- Dockerfile for easier managing _Scala_ & _Java_ versions.

Dependencies:

- [Vagrant](http://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/) 

Follow these steps to get started:

1. Git-clone this repository.

        $ git clone git@github.com:apejcic/spray-docker-vagrant-template.git my-project

2. Change directory into your clone:

        $ cd my-project

3. Install Vagrant VirtualBox guest additions sync plugin:

        $ vagrant plugin install vagrant-vbguest

4. Create vagrant box:

        $ vagrant up

5. Build docker image:

        $ vagrant ssh -c "docker build -t spray /vagrant"

6. Start the application:

        $ vagrant ssh -c "docker run -v /vagrant:/vagrant -p 8080:8080 spray"

7. Browse to http://localhost:8080/

8. Start hacking on `src/main/scala/com/example/MyService.scala`
