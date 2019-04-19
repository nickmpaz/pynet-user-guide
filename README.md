# Pynet IOT

is a simple IOT Platform for Raspberry Pis on your local network. It gives you
the ability to consume data from your devices and configure them remotely. 
Pynet is great for home automation and projects that require local remote sensing.

## Architecture

Pynet consists of 3 components: 
    
    - Gateway
    - Device Client
    - Python Module

![Pynet Architecture](https://github.com/nickmpaz/pynet-user-guide/blob/master/images/pynet.svg)

### Pynet Gateway 

The Gateway acts as a middle man between you and your devices. It is
essentially a REST API that provides endpoints for creating and consuming
devices, device data, and device configurations. The user does not need to 
interact directly with the Gateway as the Device Client and Module create
layers of abstraction on both ends.

### Pynet Device Client

### Pynet Module


