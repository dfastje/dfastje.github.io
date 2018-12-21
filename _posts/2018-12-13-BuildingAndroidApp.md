---
layout: post 
title: "Building Game Timer for Android (pending completion)" 
date: 2018-11-29
---
## Overview:  
I would like to build a more complex android app now that I have gone through the process
    of building and publishing a simple app (tic tac toe). 

## Steps with references:   

####References:
1. Timers:
    https://docs.oracle.com/javase/7/docs/api/javax/swing/Timer.html
    https://stackoverflow.com/questions/14393423/how-to-make-a-countdown-timer-in-java
2. https://stackoverflow.com/questions/5263563/linearlayout-findviewbyid-problem
3. https://projectlombok.org/features/Builder

####Steps:
#####Timer code:
I was able to lift most of this code from a stack overflow page in the references.
    I will be modifying it a little bit once I finish building out the xml for timer 
    setup!
```$xslt
public class Player {

    Timer playerTimer;
    int interval;
    int delay = 1000;
    int period = 1000;


    public Player(){

        playerTimer = new Timer();
        interval = 60;
    }

    public Player( int timeInterval ){

        playerTimer = new Timer();
        interval = timeInterval;

    }


    private void configTimer(){
        System.out.println( "The time interval is " + interval + "seconds" );
        playerTimer.scheduleAtFixedRate( new PlayerTimerTask(), delay, period);
    }

    class PlayerTimerTask extends TimerTask {

        public void run() {
            System.out.println( setInterval() );
        }
    }

    private final int setInterval(){
        if (interval == 1){
            playerTimer.cancel();
        }
        return --interval;
    }

}
```

#####Timer code:
For this code, I wanted to limit the number of android concepts that I need to learn, 
    as to not derail the entire project with learning random things 
    (I want to complete this within a couple days).
    The primary implication of this is that I will be hard coding the app to use 4 players in many locations. 



#####Random notes:
1. I couldn't get a "missing units" error to go away in the XML design page without restarting the IDE
2. There seems to be a strange delay in loading changes in the java that are made in the XML, 
    but I don't see any pending background processes.
    I have taken to breaking the code intentionally in order to have the IDE reassess the section. 