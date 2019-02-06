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
