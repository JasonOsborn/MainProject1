# MainProject1
(This is information given by one of the tutors during the verilog tutorial 2/5/19.)

Our project is as follows:

* Follow a track of magnetic tape with a cart, including 90* turns.
* On either side of the track, there will be 3 infared lights operating at 10, 100, and 1k Hz, respectively.
   * Sense these lights and stop, then deliver a notecard into a 'mailbox' waiting for it.
   * Each Hz represents one of the different mailboxes and which of the 3 cards we'll have to deliver.

Needed:

  * 3x Bandpass filter (1 for each infared light)
  * 3x Inductive sensor (1 forward, 1 left, 1 right)
  * Delivery method for the cards

---

* Track following ideas
  * Check sensors B and C (left and right) for tape. If either has it, slightly reverse, turn, and move that direction.
    * If BOTH sensor B and C, stop? Track on shown file had horizontal tape on start/stop location.
      * Maybe check if cards are still in before stopping to make sure that it doesn't immediately stop?
    * If sensor A (front or middle?) sees tape (lower priority than B or C), move forward.
    * If none of the above, reverse and check again.
  
* Infared Frequency measurement
  * Track light measurement, push through 3 bandpass filters
    * Store last 1/8th of a second of measurements, determine Hz frequency.
    * If frequency matches 10, 100, or 1k, stop, **deliver cards**.
      * Interrupts and stops track following. ('disable/enable' variable?)
