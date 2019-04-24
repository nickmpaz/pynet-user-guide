# Pynet IOT

is a simple IOT Platform for Raspberry Pis on your local network. It gives you
the ability to consume data from your devices and configure them remotely. 
Pynet is great for home automation and projects that require local remote sensing.

## Architecture

Pynet consists of 3 components: 
    
- Gateway
- Device Client
- Module

![Pynet Architecture](https://github.com/nickmpaz/pynet-user-guide/blob/master/images/pynet.svg)

### Pynet Gateway 

The Gateway acts as a middle man between you and your devices. It is
essentially a REST API that provides endpoints for creating and consuming
devices, device data, and device configurations. The user does not need to 
interact directly with the Gateway as the Device Client and Module create
layers of abstraction on both ends.

### Pynet Device Client

The Device Client powers the connection between your devices and the Gateway. 
The Client makes it easy to set up Raspberry Pi's to send sensor data to the 
Gateway and to acquire configurable values like data frequency.

### Pynet Module

The Module provides an easy way to interact with your devices and their data
from your python scripts or modules. Tasks like listing your devices become as
easy as:

    pynet.list_devices()

## Getting started

### Prerequisites

- A working Vagrant installation 
- Local wifi connection
- Raspberry Pi(s)

### Setup the Gateway

On any machine with Vagrant and a wifi connection, download the Pynet Gateway
and host it.

    $ git clone https://github.com/nickmpaz/pynet-gateway.git && cd pynet-gateway
    $ vagrant up

That's it! Ansible will do the rest. Check that the Gateway is working with:

    $ curl http://localhost:5000
    [Pynet] - Connection Successful

Make note of your host machine's hostname. Find the hostname on linux with

    $ hostname

### Setup a Raspberry Pi

Note: In this quick guide, we'll use a Device Client that sends random values to the
Gateway. Because there are a multitude of ways to outfit a Raspberry Pi with sensors, 
using them requires a little more configuration. These steps will be explained later.

FIXME v v v v v v v
get the pi set up with rasbian

download the client

.env file

do the installation process

start the client

### Interact with your Devices and their Data

from pynet import Pynet
p = Pynet()
p.resolve_connection()

now use the module to do blah blah blah

check out the docs here.

## Shutting Down & Restarting the Gateway

## Using Raspberry Pis with Sensors


