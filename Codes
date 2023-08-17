#include <Servo.h>
#include <IRremote.h>
 
unsigned long Value1 = 0xFCABFFBF; //Change these HEX codes according to your IR Remote Control.
unsigned long Value2 = 0x4CB0FADD;
 
int RECV_PIN = 11;
IRrecv irrecv(RECV_PIN);
decode_results results;
Servo servo2;
 
void setup() {
Serial.begin(9600);
irrecv.enableIRIn();
servo2.attach(9);
}

void loop() {
 if (irrecv.decode(&results)) {
 Serial.println(results.value, HEX);
 irrecv.resume();
 }
 if (results.value == Value1) {
 servo2.write(160);
 }
 else if (results.value == Value2) {
 servo2.write(70);
 }
}
