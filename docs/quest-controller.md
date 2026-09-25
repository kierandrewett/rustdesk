# Meta Quest controller input

During an Android remote session, RustDesk reads controller input delivered by Android. The left stick moves the remote cursor. The left trigger clicks the left mouse button. The right trigger clicks the right mouse button.

The stick has a dead zone to reduce movement from small hand tremors. A trigger press shorter than 70 ms sends a click. A longer press holds the mouse button until you release the trigger.

Android can report controller buttons as key events or analog input as motion events. The current implementation reads joystick axes and the standard left and right trigger axes. It also reads the `L2` and `R2` gamepad key codes.

The mapping has not been verified on a Meta Quest 3S device. It depends on Android forwarding the controller events to RustDesk. RustDesk does not map the face buttons or right stick.
