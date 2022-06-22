#include <NewPing.h>

const int trigPin = 12;
const int echoPin = 13;
 
void setup() {
pinMode(trigPin, OUTPUT);
pinMode(echoPin, INPUT);
Serial.begin(9600);
}
 
void loop()
{
long duration, cm;
 
digitalWrite(trigPin, LOW);
delayMicroseconds(2);
digitalWrite(trigPin, HIGH);
delayMicroseconds(5);
digitalWrite(trigPin, LOW);
 
duration = pulseIn(echoPin, HIGH);
 
cm = microsecondsToCentimeters(duration);
 
Serial.print(cm);
Serial.print("cm");
Serial.println();
 
delay(100);
}
 

long microsecondsToCentimeters(long microseconds)
{

}
