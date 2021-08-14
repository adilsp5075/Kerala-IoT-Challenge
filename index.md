Hi, I'm Adil S. I'm a 2nd-year Computer Science Engineering student at Government Engineering College Idukki. It's my first attempt at IoT. Hope it goes well

# Experiments

## Exp 1 : Hello World LED Blinking

### Components Required:
   * Arduino Uno Board x1
   * USB Cable x1
   * LED (Any Color) x1
   * 220 OHM Resistor X1
   * Breadboard
   * Jumper Wires (Male to Male ) x2

### Code
    int ledPin = 10; // define digital pin 10.
    void setup(){
     pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
    }
    void loop()
    {
     digitalWrite(ledPin, HIGH); // set the LED on.
     delay(1000); // wait for a second.
     digitalWrite(ledPin, LOW); // set the LED off.
     delay(1000); // wait for a second
    }


### Video
<iframe width="560" height="315" src="src/blink.mp4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


___


## Exp 2 : Traffic Light

### Components Required:
  * Arduino board x1
  * USB cable x1
  * Red M5 LED x1
  * Yellow M5 LED x1
  * Green M5 LED x1
  * 220Ω resistor x3
  * Breadboard x1
  * Breadboard jumper wires as needed

### Code
    int red =10; // initialize digital pin 8.
    int yellow =7; // initialize digital pin 7.
    int green =4; // initialize digital pin 4.
    void setup(){
     pinMode(red, OUTPUT);// set the pin with red LED as “output”
     pinMode(yellow, OUTPUT); // set the pin with yellow LED as “output”
     pinMode(green, OUTPUT); // set the pin with green LED as “output”
    }
    void loop(){
     digitalWrite(green, HIGH);//// turn on green LED
     delay(5000);// wait 5 seconds
     digitalWrite(green, LOW); // turn off green LED
     for(int i=0;i<3;i++){// blinks for 3 times
      delay(500);// wait 0.5 second
      digitalWrite(yellow, HIGH);// turn on yellow LED
      delay(500);// wait 0.5 second
      digitalWrite(yellow, LOW);// turn off yellow LED
     } 
     delay(500);// wait 0.5 second
     digitalWrite(red, HIGH);// turn on red LED
     delay(5000);// wait 5 seconds
     digitalWrite(red, LOW);// turn off red LED
    }



___

## Exp 3 : LED Chasing Effect

### Components Required:
  * LED x6
  * Arduino board x1
  * 220Ω resistor x6
  * Breadboard x1
  * USB cable x1
  * Breadboard wire x13

### Code
    int first= 2;  // the I/O pin for the first LED
    int last= 6;   // number of LEDs
    void setup(){
     for (int i = start; i < first + last; i ++){
      pinMode(i, OUTPUT);   // set I/O pins as output
     }
    }
    void loop(){
     for (int i = BASE; i < start +; i ++){
      digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
      delay(200);        // delay
    }
     for (int i = BASE; i < BASE + NUM; i ++){
      digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
      delay(200);        // delay
     }  
    }
    
    
### Video
<iframe width="560" height="315" src="src/chaser.mp4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    
    ____

<footer align="center">© 2021 Adil S </footer>
