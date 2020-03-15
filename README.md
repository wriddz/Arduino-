const int ledPin = 13; //number of LED pin
const int ldrPin = A0; //number of LDR pin

void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT); //initialise the LED pin as output
pinMode(ldrPin, INPUT); //initialise the LDR pin as input
}

void loop() {
int ldrStatus = analogRead(ldrPin); //read the status of LDR value

//check if LDR status is <=300
//if it is,LED is HIGH

if(ldrStatus<=300) {

digitalWrite(ledPin, HIGH);
Serial.println("LDR is DARK, LED is ON");
}
else {
digitalWrite(ledPin, LOW);
Serial.println("------------");
}
