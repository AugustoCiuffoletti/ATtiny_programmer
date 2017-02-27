# Programming a ATtiny84 with an Arduino Nano
Fritzing project for programming a ATtiny 84 using an Arduino Nano as a programmer

***
##HOW TO

You need an Arduino Nano, a 14 DIP socket, a strip of 30 female header connectors, a 5x7cm prototype PCB board, one LED, one 100 Ohm or higher resistor (depending on LED characteristics), a PC with the arduino IDE (version 1.6 or higher, not the one shipped with Ubuntu 16.04).

Build the board following the Fritzing design.

Upload on the Arduino Nano the "ArduinoISP" sketch, as found in the "Examples" bundled with the Arduino IDE.

Follow one of the many guides that teach how to install in the Arduino IDE the support for the ATtiny family.

Now insert the ATtiny84 and the Arduino Nano in the sockets, as indicated in the Figure.

Connect the Arduino to the PC USB socket, configure the IDE to upload to an ATtiny84 using the "Arduino as ISP" mode, and use the upload button on the IDE to flash your ATtiny with your sketch.

There is a led on board: if you use the following sketch and programming was successful it should flash:

	int led=10;
	
	void setup() {
	  pinMode(led, OUTPUT);
	}
	
	void loop() {
	  digitalWrite(led, HIGH);
	  delay(1000);
	  digitalWrite(led, LOW);
	  delay(2000);
}
