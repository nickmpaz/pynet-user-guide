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
It makes it easy to set up Raspberry Pi's to send sensor data to the
Gateway and to acquire configurable values like data frequency.

### Pynet Module

The Module provides an easy way to interact with your devices and their data
from your python scripts or modules. With the Module, a task like listing your
devices becomes as easy as:

    pynet.list_devices()


