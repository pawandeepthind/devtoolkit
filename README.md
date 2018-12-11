# What

Dev machine for IBM CoC Integrated DevToolKit. This create CentOS 7 with pre-requisite software.

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
    * Machine is setup with software using [ansible](https://www.ansible.com/).
    * Machine names,port forwarding and memory can be configured using config.xml

## Setup devtoolkit

  If it is desired to setup the Docker-based integrated developer toolkit along with the VM creation,
    * Use IBM UrbanCode Deploy Selfserv tool to download the IBM OMS Integrated Development Toolkit
    * Download the devtoolkit_docker.tar to {PWD}/server/roles/files directory.

## SSH into machine

  Once machines are up, user can ssh into the machine using
  ```
    $ vagrant ssh dev
  ```

## Coming Soon

  * Ansible playbook for usual operations like 
    * Setup for extension deployment
    * Setup for building the customization
    * Setup for CDT build