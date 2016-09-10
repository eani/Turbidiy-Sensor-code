# Turbidiy-Sensor-code
/* 
This arduino code is to be used to get the reading of a turbidity sensor
Since the Turbidity Sensor is a analog sensor, there is no need to import any extra libries.
All you need is to connect the analog sensor to any on the analog pin of the arduino board.
*/


void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(9600);
}

// the loop routine runs over and over again forever:
void loop() {
  Serial.println("Taking Readings from turbidity Sensor");
  delay(4000);
  int turbidityValue = analogRead(A1);
  float turbidityV = turbidityValue/100;
  Serial.print("Turbidity level: ");
  Serial.println(turbidityV);

}
