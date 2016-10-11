# [Myo-OSC](http://samy.pl/myo-osc/)

OSC bridge for Thalmic Myo gesture control armband for Windows and Mac OS X 10.8+.

Originally By [Samy Kamkar](http://samy.pl)

This version by Michele Abolaffio (micheleabolaffio.wordpress.com)

Myo-OSC is a C++ application designed to take hand gestures, accelerometer, gyroscope and magnetometer data from the [Thalmic Labs Myo](https://www.thalmic.com/en/myo/) armband and output it over OSC. This allows incredible control of virtually any device or application just by waving or flailing your arm or hand around like a madman.


You can also send any OSC data over a network.

Original branch on [github](http://samy.pl/myo-osc/)

------

## Usage
$ ./myo-osc [IP address (default: 127.0.0.1)] [OSC port (default: 7777)]

This will output the following OSC data

```
/myo/pose s ID s pose

/myo/accel s ID f X_vector3 f Y_vector3 f Z_vector3

/myo/gyro s ID f X_vector3 f Y_vector3 f Z_vector3

/myo/orientation s ID f roll f pitch f yaw

/myo/orientationQuat s ID f X_quaternion f Y_quaternion f Z_quaternion f W_quaternion
```



Examples:

```
/myo/pose s 0 s fist

/myo/accel s 0 f 0.95849609375 f 0.26953125 f 0.20068359375

/myo/gyro s 0 f -7.14111280441284 f -15.8081045150757 f 5.43212842941284

/myo/orientation s 0 f 0.928672909736633 f -1.23411226272583 f 1.45198452472687

/myo/orientationQuat s 0 f -0.00215625390410423 f 3.37712929902281e-43 f -0.0021759606897831 f 0
```


------

### Software

#### Myo-OSC
This software.

#### oscpack
We also use [oscpack](https://code.google.com/p/oscpack/), a C++ OSC (Open Sound Control) library.

### Hardware



## Main changes

This version of myo-osc is specifically tailored to work in a performative environment. It is hardcoded to respond to the mac addresses of the two myos that I use, recognising them and outputting their custom ID in every OSC message. 
If you find it useful download it and modify the function identifyMAC to respond to the MAC addresses of your device. 
You can find the MAC address of the myo easily by visiting http://diagnostics.myo.com/


Feel free to contact me with any questions!

You can reach me at <michele.abolaffio@gmail.com>.
Or you can check my work at <micheleabolaffio.wordpress.com>

Remember to follow [@SamyKamkar](https://twitter.com/samykamkar) on Twitter or check out <http://samy.pl> for his other projects.
