# AlwaysAI-JetsonNano-CUDA-ObjectDetection
An example of the AlwaysAI Object Detection "Getting Started App", running in a container, to be deployed via balena.  Intended for use on an Nvidia Jetson Nano, with a USB webcam attached.

## Running this Demo
Simply perform a 

`git clone https://github.com/balenalabs-incubator/AlwaysAI-JetsonNano-CUDA-ObjectDetection.git` 

on this repository. Then, from within the directory on your local machine, perform a 

`balena push YourApplicationNameHere`

Or, even easier, you can use our new "Deploy with Balena" button!  Simply click this:

[![](https://www.balena.io/deploy.png)](https://dashboard.balena-cloud.com/deploy)

You will be asked to create an account at Balena if you do not already have one, login to your account if you do, or, be taken directly to an App deployment if you are already logged in.  This Repo is only designed for a Jetson Nano, so choose that from the drop-down menu of device types, and click the "Create and deploy" button.  This will create a container build on our balenaCloud infrastructure that runs in the background, of the AlwaysAI container.  Your device will download that container in just a bit.

Next, you need to add a Device.  Click the "Add Device" button at the top.  On the modal, if you will be using WiFi then toggle the switch to enable WiFi + Ethernet, and add your WiFi credentials (these are passed to the device, not stored on balenaCloud).  At the bottom, click "Download" and your OS will be downloaded to your laptop or desktop.  This OS image needs to be flashed to an SD Card, and once that is complete, you can insert into your Jetson Nano and power up (make sure you are using the barrel jack power adapter, the micro-USB power adapter will not provide enough power).

In a few moments, it will come online, you will see it in your balenaCloud dashboard, and the device will begin downloading the AlwaysAI container that was being built in the backgound.

Finally, on the Device Details page, take note of the device's IP Address.  AlwaysAI uses port 5000, so if you browse to `http://<insert-ip-address-here>:5000` you should see AlwaysAI running!
