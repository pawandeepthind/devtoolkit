# What

Dev machine for IBM CoC Integrated DevToolKit. This create CentOS 7 with pre-requisite software. System consist of two machines
  
  * __manager__ - machine that will help in installing all the pre-requisites and commands.
  * __dev__     - machine that will host the actual toolkit.

# How

## 1. Install Pre-requisite:

It is good to read about Vagrant and Ansible.

## Here are some of the pre-requisite (Note: It is tested on Mac OS X for now)

  * Latest vagrant
  * Latest Virtual Box
  * Checkout the repository code locally
  * Open command prompt (for windows i will recomment to use [gitbash](https://gitforwindows.org/))
  * Change directory where the code is checked out.
  * Install plugins (vbguest and hostmanager)
    ```
      $ vagrant plugin install vagrant-vbguest
      $ vagrant plugin install vagrant-hostmanager
    ```
  * After installation of the plugins do 
    ```
      $ vagrant up
    ```
  * Note: 
    * Machine is setup with software using [ansible](https://www.ansible.com/) that is installed on manager.
    * Machine names,port forwarding and memory can be configured using config.xml

## SSH into machine

  Once machines are up, user can cd to the directory where the repository code is checked out and try vagrant ssh {machinename} i.e. vagrant ssh dev/manager
  ```
    $ vagrant ssh dev
  ```

## Coming Soon

  * Commands to enable 
    * Setup of downloaded devtoolkit_docker.tar
    * Setup for extension deployment
    * Setup for building the customization
    * Setup for CDT build