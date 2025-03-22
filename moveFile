#include <Stepper.h>
#define steps 20  // Количество шагов на один оборот
#define f1 A0
#define f2 A1
#define f3 A2
#define f4 A3
#define f5 A4
#define f6 A5
#define f7 A6
#define f8 A7
// 1 оборот - ~1000
int f[8][8] = { 0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0,
                0, 0, 0, 0, 0, 0, 0, 0 };
/*int poisk(int f[8][8]){
  for (int i; i<8; i++){
    for (int j; j<8; j++){
      if()
    }
  }
}*/
Stepper od(steps, 35, 5);
Stepper oz(steps, 34, 4);
Stepper oy(steps, 33, 3);
Stepper ox(steps, 32, 2);
void find0y() {  //true
  onOy();
  while (digitalRead(47)) {
    oy.step(steps);
  }
}
void offDrivers() {
  digitalWrite(24, 1);
  digitalWrite(25, 1);
  digitalWrite(22, 1);
  digitalWrite(23, 1);
}
void onOz() {
  digitalWrite(24, 0);
  digitalWrite(25, 1);
  digitalWrite(22, 1);
  digitalWrite(23, 1);
}
void onOd() {
  digitalWrite(24, 1);
  digitalWrite(25, 0);
  digitalWrite(22, 1);
  digitalWrite(23, 1);
}
void onOx() {
  digitalWrite(24, 1);
  digitalWrite(25, 1);
  digitalWrite(22, 0);
  digitalWrite(23, 1);
}
void onOy() {
  digitalWrite(24, 1);
  digitalWrite(25, 1);
  digitalWrite(22, 1);
  digitalWrite(23, 0);
}
void find0x() {  //true
  onOx();
  while (digitalRead(48)) {
    ox.step(steps);
  }
}
void find00() {
  find0y();
  find0x();
}

void find0d() {  //true
  onOd();
  while (digitalRead(46)) {
    od.step(-steps);
  }
}
void find0d2() {  //true
  onOd();
  while (digitalRead(45)) {
    od.step(steps);
  }
}
void find0z_down() {
  onOz();
  while (digitalRead(43)) {
    oz.step(-steps);
  }
}
void find0z_up() {
  onOz();
  while (digitalRead(44)) {
    oz.step(steps);
  }
}
void find0d_2() {  //true
  onOd();
  while (digitalRead(45)) {
    od.step(steps);
  }
}
void onMagnet() {
  digitalWrite(51, 0);
}
void offMagnet() {
  digitalWrite(51, 1);
}
void setup() {

  //od.setSpeed(1000);
  pinMode(44, INPUT);
  pinMode(51, OUTPUT);
  pinMode(46, INPUT);
  pinMode(22, INPUT_PULLUP);
  pinMode(23, OUTPUT);
  pinMode(24, INPUT_PULLUP);
  pinMode(25, INPUT_PULLUP);
  pinMode(26, INPUT_PULLUP);
  pinMode(27, INPUT_PULLUP);
  pinMode(28, INPUT_PULLUP);
  pinMode(29, INPUT_PULLUP);
  pinMode(30, INPUT_PULLUP);
  pinMode(31, INPUT_PULLUP);
  pinMode(48, INPUT);
  pinMode(50, INPUT);
  pinMode(42, INPUT);
  pinMode(43, INPUT);
  pinMode(47, INPUT);
  //digitalWrite(51,1);
  Serial.begin(9600);
  pinMode(A15, INPUT);
  pinMode(45, INPUT);
  pinMode(52, OUTPUT);
  pinMode(53, OUTPUT);
  pinMode(22, OUTPUT);
  pinMode(23, OUTPUT);
  pinMode(24, OUTPUT);
  pinMode(25, OUTPUT);
  //digitalWrite(23,0);
  // digitalWrite(51, 1);
  /*od.setSpeed(1023);
  oz.setSpeed(1023);
  ox.setSpeed(1023);
  oy.setSpeed(1023);*/
  od.setSpeed(32000);
  oz.setSpeed(32000);
  ox.setSpeed(32000);
  oy.setSpeed(32000);
  offMagnet();
  find00();
  find0d();
  find0z_up();
  offDrivers();
}
int x = -550;  // сеолько доехать до 1 вертикали
int stepY = -3000;
int otstupY = -500;
void gotoA() {
  onOy();
  oy.step(-600);
}
void gotoB() {
  onOy();
  oy.step(stepY * 1);
}
void gotoC() {
  onOy();
  oy.step(stepY * 2 - otstupY);
}
void gotoD() {
  onOy();
  oy.step(stepY * 3 - otstupY * 2 + 500);
}
void gotoE() {  //false
  onOy();
  oy.step(stepY * 4 - otstupY * 3.7);
}
void gotoF() {  //false
  onOy();
  oy.step(stepY * 4 - 500);
}
void gotoG() {
  onOy();
  oy.step(-15200);
}
void gotoH() {  //true
  onOy();
  oy.step(-17400);
}
void goto1() {  //true
  onOx();
  ox.step(-8500 - 2430 * 0);
}
void goto2() {
  onOx();
  ox.step(-8500 - 2430 * 1);
}
void goto3() {
  onOx();
  ox.step(-8500 - 2430 * 2);
}
void goto4() {
  onOx();
  ox.step(-8500 - 2430 * 3);
}
void goto5() {
  onOx();
  ox.step(-8000 - 2430 * 4);
}
void goto6() {
  onOx();
  ox.step(-8500 - 2430 * 5);
}
void goto7() {
  onOx();
  ox.step(-8500 - 2430 * 6);
}
void goto8() {  //true
  onOx();
  ox.step(-8000 - 2430 * 7);  //-25 500
}
void xod(char let, int n, bool mag = 0) {
  find00();
  if (let == 'A') {
    gotoA();
  }
  if (let == 'B') {
    gotoB();
  }
  if (let == 'C') {
    gotoC();
  }
  if (let == 'D') {
    gotoD();
  }
  if (let == 'E') {
    gotoE();
  }
  if (let == 'F') {
    gotoF();
  }
  if (let == 'G') {
    gotoG();
  }
  if (let == 'H') {
    gotoH();
  }
  if (n == 1) {
    goto1();
  }
  if (n == 2) {
    goto2();
  }
  if (n == 3) {
    goto3();
  }
  if (n == 4) {
    goto4();
  }
  if (n == 5) {
    goto5();
  }
  if (n == 6) {
    goto6();
  }
  if (n == 7) {
    goto7();
  }
  if (n == 8) {
    goto8();
  }
  if (mag) {
    onMagnet();
  } else {
    offMagnet();
  }
}
void ozDownForRearrangement() {
  onOz();
  oz.step(-30000);
  offDrivers();
}
void xodFromTo(char oldLet, int oldN, char newLet, int newN) {
  find00();
  find0z_up();
  xod(oldLet, oldN, 1);
  delay(2000);
  ozDownForRearrangement();
  xod(newLet, newN, 1);
  find0z_up();
  offMagnet();
  offDrivers();
  delay(2000);
}
void xodFinal(char oldLet, int oldN, char newLet, int newN) {
  find0z_down();
  find0d_2();
  offDrivers();
  while (!digitalRead(42)) {}
  find0d();
  find0z_up();
  while(!digitalRead(42)){}
  xodFromTo(oldLet, oldN, newLet, newN);
  find00();
  while(!digitalRead(42)){}
  find0z_down();
  find0d_2();
  offDrivers();
}
void loop() {
  /*if(digitalRead(42)){
    digitalWrite(51,0);
  }
  else{
    digitalWrite(51,1);
  }*/
  // for magnet tests

  if (digitalRead(42)) {
    xodFinal('F', 5, 'D', 5);
  }
  // gotoH();
  // goto1();
  // find00();
  // if (digitalRead(42)) {
  //   gotoA();
  //   goto8();
  // }
  // while(1){}
}
