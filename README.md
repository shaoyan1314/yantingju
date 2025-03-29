# 颜廷举

#include <stdio.h>

// 递归函数计算斐波那契数列
int fibonacci(int n) {
    if (n == 0)
        return 0;
    if (n == 1)
        return 1;
    return fibonacci(n - 1) + fibonacci(n - 2);
}

int main() {
    int n = 10;  // 这里可以修改n的值来获取不同位置的斐波那契数
    int result = fibonacci(n);
    printf("The %d - th Fibonacci number is %d\n", n, result);
    return 0;
}
#include <Servo.h>

String num;
String my_num;
Servo servo_PA0;

boolean digitalRead(uint8_t pin) {
  pinMode(pin, INPUT);
  boolean _return =  digitalRead(pin);
  pinMode(pin, OUTPUT);
  return _return;
}

void setup(){
  num = "12345";
  my_num = "";
  servo_PA0.attach(PA0);
  pinMode(PA10, OUTPUT);
  servo_PA0.write(0);
  delay(100);
  digitalWrite(PA10,LOW);
  Serial.begin(9600);
}

void loop(){
  if (digitalRead(PA1) == 0) {
    my_num = String(my_num) + String("1");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

  if (digitalRead(PA2) == 0) {
    my_num = String(my_num) + String("2");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

  if (digitalRead(PA3) == 0) {
    my_num = String(my_num) + String("3");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

  if (digitalRead(PA8) == 0) {
    if (my_num == num) {
      pinMode(PA10, OUTPUT);
      tone(PA10,220);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,247);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,131);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,147);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,165);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,165);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,175);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      pinMode(PA10, OUTPUT);
      tone(PA10,196);
      delay(100);
      pinMode(PA10, OUTPUT);
      noTone(PA10);
      servo_PA0.write(180);
      delay(100);
      servo_PA0.write(0);
      delay(100);

    } else {
      pinMode(PA10, OUTPUT);
      tone(PA10,880);
      delay(2000);
      pinMode(PA10, OUTPUT);
      noTone(PA10);

    }
    my_num = "";
    Serial.println(my_num);

  }

  if (digitalRead(PA7) == 0) {
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    my_num = "";
    Serial.println(my_num);

  }

  if (digitalRead(PA4) == 0) {
    my_num = String(my_num) + String("4");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

  if (digitalRead(PA5) == 0) {
    my_num = String(my_num) + String("5");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

  if (digitalRead(PA6) == 0) {
    my_num = String(my_num) + String("6");
    pinMode(PA10, OUTPUT);
    tone(PA10,131);
    delay(100);
    pinMode(PA10, OUTPUT);
    noTone(PA10);
    Serial.println(my_num);

  }

}
