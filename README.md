# Terraform Cloud Agent Docker Images

A collection of Dockerfiles for building custom Terraform Cloud Agent images based on the official HashiCorp image. 

The Dockerfiles are placed within the subdirectories and typically add a single tool to the image.

**Note:** The Dockerfiles will use the latest Terraform Cloud Agent container image and so different builds of the same file may result in an image having different version of the Terraform Cloud Agent.

## Vagrant environment

The project includes a vagrant file that will bring up a Linux VM with docker-ce installed, which can be used for building the images.

To use it:

* Have VirtualBox installed
* Have Vagrant installed
* Start the VM with Vagrant

  ```bash
  vagrant up
  ```

* Login to the VM

  ```bash
  vagrant ssh
  ```
* Change to the shared directory, where the repository files will be available inside the VM.

  ```bash
  cd /vagrant
  ```
* Destroying the VM

  ```bash
  vagrant destroy
  ```