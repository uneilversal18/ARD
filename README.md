const int buttonPin = 2;
const int buzzerPin  = 4;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  
  if (digitalRead(buttonPin) == LOW) {
    digitalWrite(buzzerPin, HIGH);
    Serial.println("Good Job");
    delay(1000);
    digitalWrite(buzzerPin, LOW);
    delay(500);
  }
}
