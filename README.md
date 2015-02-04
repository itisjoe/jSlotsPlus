# jSlotsPlus

ver 0.2

based on jSlots ( matthewlein/jQuery-jSlots )

## Options

        $.jSlots.defaultOptions = {
            number : 3,          // Number: number of slots
            winnerNumber : 1,    // Number or Array: list item number(s) upon which to trigger a win, 1-based index, NOT ZERO-BASED
            spinner : '',        // CSS Selector: element to bind the start event to
            spinEvent : 'click', // String: event to start slots on this event
            onInit : $.noop,     // Function: runs on init,
            onStart : $.noop,    // Function: runs on spin start,
            onEnd : $.noop,      // Function: run on spin end. It is passed (finalNumbers:Array). finalNumbers gives the index of the li each slot stopped on in order.
            onWin : $.noop,      // Function: run on winning number. It is passed (winCount:Number, winners:Array, finalNumbers:Array)
            easing : 'swing',    // String: easing type for final spin. I recommend the easing plugin and easeOutSine, or an easeOut of your choice.
            time : 7000,         // Number: total time of spin animation
            loops : 6            // Number: times it will spin during the animation
            result : {},         // object: set result, like {0:7, 1:6, 2:5} will get 765

        };

## what is new

1. Add a parameter "result", it can set a regular number instead of a random number.

        result : {0:7, 1:6, 2:5}

    It will display "765", more or less is fine.

2. Add a method "onInit"
3. Result numbers can be changed.

        var jsSlot = $('.slot').jSlotsPlus({
            result: {0:7,1:6,2:5}
        })[0];
        
        // if u want to change result numbers
        jsSlot.options.result = {0:1,1:2,2:3};


Other usage details please visit [https://github.com/matthewlein/jQuery-jSlots](https://github.com/matthewlein/jQuery-jSlots)
