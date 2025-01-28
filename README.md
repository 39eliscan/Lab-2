# Lab-2
// the setup routine runs once when you press reset:
const int ledPin = 2;

void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(9600);

  
  pinMode(ledPin, OUTPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  // read the input on analog pin 0:
   // print out the value you read:

  int sensorValue = analogRead(A0);

  Serial.println(sensorValue);

  if (sensorValue > 400) {
  
   digitalWrite(ledPin, HIGH);
  } else {
  
    digitalWrite(ledPin, LOW);
  }



}
