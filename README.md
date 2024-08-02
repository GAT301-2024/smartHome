# SMART HOME.

NAMASABA BRIDGET 23/U/2232/GIM/PS.

Automatic Door Opener with Ultrasonic Sensor and Buzzer.

Overview;

This project demonstrates an automatic door opener using an Arduino, an ultrasonic sensor, a servo motor, and a buzzer. The ultrasonic sensor detects the presence of an object within a specified distance, triggering the buzzer and opening the door via the servo motor.

Components;

    Arduino board
    Ultrasonic sensor (HC-SR04)
    Servo motor
    Buzzer
    Jumper wires

Circuit Diagram;

    Trig Pin: Connected to digital pin 13
    Echo Pin: Connected to digital pin 9
    Servo Pin: Connected to digital pin 7
    Buzzer Pin: Connected to digital pin 5

How It Works;

    Setup:
        Initialize the serial communication at 9600 baud rate.
        Attach the servo motor to the specified pin.
        Set the pin modes for the trig pin, echo pin, and buzzer pin.
        Initialize the servo motor to the closed position (0 degrees).

    Loop:
        Trigger the ultrasonic sensor and measure the duration of the echo pulse.
        Calculate the distance based on the duration.
        Print the distance to the serial monitor.
        If an object is detected within 15 cm:
            Activate the buzzer for 2 seconds.
            Open the door by setting the servo motor to 90 degrees.
        If no object is detected within 15 cm:
            Print a message indicating no nearby object.
            Close the door by setting the servo motor to 0 degrees.
        Wait for 1 second before the next loop iteration.

Notes;

    Adjust the distance threshold (15 cm) as needed for your specific application.
    Ensure proper wiring and power supply for the servo motor and buzzer to avoid damaging the components.
