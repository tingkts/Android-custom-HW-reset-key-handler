Custom HW reset key behavior

Custom HW reset key's handler to perform factory reset.

* press THE reset key and keep hold on till two seconds: show UI Toast to inform user that If you continue to press for 5 seconds, it will go directly to the factory to reset.
  
* Corresponding to the above, if user have pressed the HW reset key for 7 seconds, go directly to the factory reset mode.


Behavior use case

use case 1 : screen on, stay in Launcher,

    press HW reset key,

    hold for 2 seconds: show Toast.

    hold for 7 seconds: perform factory reset directly

    During the entire process screen lights up and does not enter the dark screen standby state.


use case 2 : screen on , stay in Launcher, no settings of Keyguard lock, screen turn off by auto timeout of no user activity

    press HW reset key : screen will be turned on, and keep on.

    hold for 2 seconds: show Toast.

    hold for 7 seconds: perform factory reset directly

    After pressing HW reset key, screen lights up and does not enter the dark screen standby state.


use case 3 : screen on , stay in Launcher, has Keyguard lock settings, screen turn off by auto timeout of no user activity

    press HW reset key : screen will be turned on, and keep on, but stay in Keyguard lock screen.

    hold for 2 seconds: show Toast in background. (occluded by Keyguard)

    hold for 7 seconds: perform factory reset directly

    After pressing HW reset key, screen lights up and stay in Keyguard lock scrren, then screen will turn off by auto timeout of user activity monitor. 


The patches is in aosp_p_9.0.0 which is based on android P (9.0.0).