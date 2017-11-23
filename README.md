# [Myo-OSC](http://samy.pl/myo-osc/)

OSC bridge for Thalmic Myo gesture control armband for Windows and Mac OS X 10.8+.

Originally By [Samy Kamkar](http://samy.pl)

This version by Michele Abolaffio (micheleabolaffio.wordpress.com)

Myo-OSC is a C++ application designed to take hand gestures, accelerometer, gyroscope and magnetometer data from the [Thalmic Labs Myo](https://www.thalmic.com/en/myo/) armband and output it over OSC. This allows incredible control of virtually any device or application just by waving or flailing your arm or hand around ike a crazy person.


You can also send any OSC data over a network.

Original branch on [github](http://samy.pl/myo-osc/)

------

## Usage
$ ./myo-osc [IP address (default: 127.0.0.1)] [OSC port (default: 7777)]

This will output the following OSC data

```
/myo/pose i ID s pose

/myo/accel i ID f X_vector3 f Y_vector3 f Z_vector3

/myo/gyro i ID f X_vector3 f Y_vector3 f Z_vector3

/myo/orientation i ID f roll f pitch f yaw

/myo/orientationQuat i ID f X_quaternion f Y_quaternion f Z_quaternion f W_quaternion

/myo/emg i ID i EMG[0], i EMG[1], i EMG[2], i EMG[3], i EMG[4], i EMG[5], i EMG[6], i EMG[7]


```



Examples:

```
/myo/pose, 0, fist

/myo/accel, 1, -0.0263671875, 0.52099609375, 0.56884765625

/myo/gyro, 1, -9.3125, -0.3125, 11.3125

/myo/orientation, 1, 0.78527563810349, 0.15019522607327, -2.9084701538086

/myo/orientationQuat, 1, -0.11322021484375, 0.37091064453125, 0.9183349609375, -0.07861328125

/myo/emg, 1, 4, -11, -6, -11, -12, -3, 14, 5

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
The myos are permanently unlocked and will not vibrate for any pose recognised.
If you find it useful download it and modify the function identifyMAC to respond to the MAC addresses of your device. 
You can find the MAC address of the myo easily by visiting http://diagnostics.myo.com/


Feel free to contact me with any questions!

You can reach me at <michele.abolaffio@gmail.com>.
Or you can check my work at micheleabolaffio.wordpress.com

Remember to follow [@SamyKamkar](https://twitter.com/samykamkar) on Twitter or check out <http://samy.pl> for his other projects.
