# Arduino-Vibration-using-UltraSonic-sensor
Now this project is all about vibrating a vibrating motor through Arduino with the help of ultrasonic sensor.  
// defines pins numbers
 const int trigPin=2;
 const int vibPin=10;
 const int vibPin2=9;
 const int echoPin=3;
 const int ledpin1=6;
 const int ledpin2=7;
 


// defines variables
long duration;
int distance;



void setup() {
pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output
pinMode(echoPin, INPUT);
pinMode(vibPin, OUTPUT);
pinMode(vibPin2, OUTPUT);
Serial.begin(9600); // Starts the serial communication
}



void loop() 
{
  // Clears the trigPin
  digitalWrite(trigPin, LOW);
  delayMicroseconds(10);

  // Sets the trigPin on HIGH state for 10 micro seconds
  digitalWrite(trigPin, HIGH);
  digitalWrite(trigPin, LOW);
  

  // Reads the echoPin, returns the sound wave travel time in microseconds
    duration = pulseIn(echoPin, HIGH);
    distance= duration*0.034/2;

  // Prints the distance on the Serial Monitor
    Serial.print("Distance: \t");
    Serial.println(distance);
  if(distance<=10)
  {
   Serial.println("object is near");
    digitalWrite(vibPin, LOW);
    digitalWrite(vibPin2, LOW);
    digitalWrite(ledpin1, LOW);   //glowing led lights
     delay(500);
    digitalWrite(ledpin2, LOW);   //glowing led lights
    delay(500);
  }
  else if(distance<=100)
  {
    Serial.println("Object detected");
     digitalWrite(vibPin, HIGH);
     digitalWrite(vibPin2, HIGH);
     digitalWrite(ledpin1, HIGH); //glowing led lights
     delay(500);
     digitalWrite(ledpin2, HIGH);   //glowing led lights
     delay(500);
  }
  else
  {
    digitalWrite(vibPin, LOW);
    digitalWrite(vibPin2, LOW);
    digitalWrite(ledpin1, LOW); //glowing led lights
     delay(500);
     digitalWrite(ledpin2, LOW);  //glowing led lights
     delay(500);
    Serial.println("Object is far away");
  }
 }
