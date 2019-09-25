*This is a copy of the original introductory post from our [forum](https://forum.makeit.zone/t/element-14-micro-bit-summer-of-code-club-challenge-2019) and also published to [Element14](https://www.element14.com/community/community/stem-academy/microbit/blog/2019/08/07/makeitzone-microbit-soccc-2019-blog-1-project-outline)*.

# MicroBit-LockBox-Challenge

Element14 Summer of Code 2019 Microbit Challenge

We were very lucky to be selected as winners of Element14's [Micro:Bit Summer Code Club Challenge](https://www.element14.com/community/docs/DOC-92809/l/microbit-summer-code-club-challenge-winners-announced#comment-159305)!

To help us bring coding to our community we received:

- a [micro:bit Club Pack](https://uk.farnell.com/bbc-micro-bit/mb224/bbc-micro-bit-club/dp/2728766?ICID=microbit-club&COM=Documents)
- 5 x [Kitronik Inventor kits](https://uk.farnell.com/kitronik/5603/inventor-kit-micro-bit/dp/2563847?st=kitronik%20inventor%20kit&COM=Documents)

The challenges I set myself for this code club were:

- any age, including adults
- scalable in both number of participants, and complexity
- fun!

The final idea:

**An electronic puzzle/escape room device.**

## System Outline

### Lock Box
There will be a central "lock box" to which the "lock-master" micro:bit will be connected.
The lock box will be any container that can be secured in such a way that a servo can be used to "unlock". The box will contain some sort of reward or prize for participants.

It will be programmed to listen on a known [radio](https://makecode.microbit.org/reference/radio) group.

There will be an *admin* mode that allows the mentor running the session to adjust the number of **puzzle bits** being used.

The lock-master awaits messages from the puzzle-bits that indicate they have been solved. When all puzzle bits are solved, the servo is activated and the lock-box unlocked.

#### Things to Consider
Cheating. The initial code will probably just wait for 5 "unlocked" messages. 
This can be enhanced:
- check the serial number sent from each micro:bit
- an initial "setup" stage that records the serials of the "allowed" puzzle-bits

Suggestion: leave it open, have a discussion about hacking, let participants try to hack, secure, and hack again :-)

### Puzzle Bits
These are the micro:bits that participants will work with.

They will be provided with a template that includes the steps needed to send the "puzzle solved" message to the lock-master.

Participants then create a puzzle (as simple or as complicated as they like) for a user to solve. 

## Session Outline

Minimum session time: 2 hours.

- welcome
- brief description of micro:bit
- show maker:code
- download basic "press button->message" example
   - verify download is working with known good code
- go over basic loops and logic
  - practice
- go over displaying messages
  - practice
- introduce the sensors
  - practice. Potentially limit sensors covered if time is short.
- Challenge: Come up with a puzzle for a person to solve on your micro:bit
  - introduce template code that sends "solved" message to master
- Wrap up:
  - swap puzzle-bits with other participants, see if group can unlock the lock box and earn the reward!

## Extensions
- movement based puzzles (accelerometer, compass)
- physical inputs (switches, LDR, etc)
- other sensors
- connecting to more advanced computers (eg puzzle on Raspberry Pi, BrainPad Arcade, ...)

## Rewards
- location of a cooler full of ice blocks, etc
- discount coupons to an escape room (working on that for Courtenay.)
