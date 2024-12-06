# Home-automation-using-Relay
// C++ code
//
int pir_sensor = 0;

void setup()
{
  pinMode(A0, INPUT);
  Serial.begin(9600);
  pinMode(7, OUTPUT);
}

void loop()
{
  pir_sensor = analogRead(A0);
  Serial.println(pir_sensor);
  if (pir_sensor >= 100) {
    digitalWrite(7, HIGH);
    delay(2000); // Wait for 2000 millisecond(s)
  } else {
    digitalWrite(7, HIGH);
  }
}
