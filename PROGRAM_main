// Motor control pins
const int IN1 = 2;
const int IN2 = 3;

// Button pins
const int buttonForward = 4;
const int buttonBackward = 5;

void setup() {
  // Set motor pins as output
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);

  // Set button pins as input
  pinMode(buttonForward, INPUT);
  pinMode(buttonBackward, INPUT);
}

void loop() {
  bool forward = digitalRead(buttonForward);
  bool backward = digitalRead(buttonBackward);

  if (forward && !backward) {
    // Rotate motor forward
    digitalWrite(IN1, HIGH);
    digitalWrite(IN2, LOW);
  } 
  else if (!forward && backward) {
    // Rotate motor backward
    digitalWrite(IN1, LOW);
    digitalWrite(IN2, HIGH);
  } 
  else {
    // Stop motor
    digitalWrite(IN1, LOW);
    digitalWrite(IN2, LOW);
  }
}
