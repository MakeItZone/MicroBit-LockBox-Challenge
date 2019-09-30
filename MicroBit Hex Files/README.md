These files can be directly loaded into [MakeCode for MicroBit](https://makecode.microbit.org).

* [microbit-master-lockbox.hex](microbit-master-lockbox.hex) - is the "master" control program to be installed into the MicroBit attached to the "safe". 
* [microbit-sample-puzzlebit.hex](microbit-sample-puzzlebit.hex) - is a skeleton "puzzlebit" application that shows how to send `lock` and `unlock` messages to the "safe."
* [microbit-basic-compass-puzzlebit.hex](microbit-basic-compass-puzzlebit.hex) - a very simple PuzzleBit that must be turned to face a certain direction and also have the "A" key pressed to send the `unlock` message.

There are also PDF "print outs" of each of the programs.

## Master Safe Program

When run/reset you can configure the number of "PuzzleBits" by pressing the `A` and `B` keys.

Let's call the number of PuzzleBits `N`.

Press `A+B` to move to the running state.

As each PuzzleBit sends `unlock` or `lock` the servo will move by the `1/N * rotation required to open the lock`. 

There is also a *Konami-style* code (`A-B-B-A`) that will override the current lock position and open the safe. Press `A+B` to return to the normal running state.

In the running state, `A+B` will reset back to the `configuration` state.

You will most likely need to adjust the `minimum` and `maximum` servo angles in the code to match your servo motor.
