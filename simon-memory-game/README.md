# Arduino Simon Memory Game

## Overview
A microcontroller-based memory game inspired by the classic Simon. The system generates random LED sequences that the user must reproduce using push-buttons.

## Hardware
- Arduino Uno
- Push buttons
- LEDs + resistors
- Buzzer

## Features
- Randomized pattern generation
- Button debouncing logic
- State-machine driven gameplay
- Audio-visual feedback

## Skills Demonstrated
- Embedded state machine design  
- GPIO input handling  
- Timing and control logic

## Media
<img width="369" height="263" alt="image" src="https://github.com/user-attachments/assets/38720f18-0add-4518-8d31-6fd7cefc20ef" /><img width="369" height="263" alt="image" src="https://github.com/user-attachments/assets/dfba6c20-42fc-474b-a3d9-7276aef1d0fe" /> 

## Game Code

delay(400);
for(byte i=0;i<level;i++){
  digitalWrite(ledPin[seq[i]],HIGH);
  tone(10,toneHz[seq[i]],300);
  delay(300);
  digitalWrite(ledPin[seq[i]],LOW);
  noTone(10);
  delay(180);
}

for(byte i=0;i<level;i++){
  int pressed=-1;

  while(pressed==-1){
    for(byte b=0;b<N;b++){
      if(digitalRead(btnPin[b])==LOW){
        delay(20);
        while(digitalRead(btnPin[b])==LOW);
        delay(20);
        pressed=b;
      }
    }
  }

  digitalWrite(ledPin[pressed],HIGH);
  tone(10,toneHz[pressed],200);
  delay(200);
  digitalWrite(ledPin[pressed],LOW);
  noTone(10);

  if(pressed!=seq[i]){
    for(byte k=0;k<3;k++){
      for(byte j=0;j<N;j++) digitalWrite(ledPin[j],HIGH);
      tone(10,150,300);
      delay(300);
      for(byte j=0;j<N;j++) digitalWrite(ledPin[j],LOW);
      noTone(10);
      delay(250);
    }
    while(true){
      for(byte b=0;b<N;b++){
        if(digitalRead(btnPin[b])==LOW){
          delay(50);
          while(digitalRead(btnPin[b])==LOW);
          delay(50);
          return;
        }
      }
    }
  }
}

