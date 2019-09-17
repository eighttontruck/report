시나리오 : 오늘 배운 아두이노 조도센서를 이용해 일반 가정집에 접목하여 밖이 어두워지면 자동으로 불이켜지는 회로를 만들고 싶습니다.
지붕 위에 달아 아침일땐 불이
꺼지고 어두워 지면 켜지는 센서등을 생각해 보았습니다.

소감 : 3주차 창의공학 수업으로 아두이노 조도 센서를 이용한 회로를 만들어봤는데 아두이노의 흥미를 느꼈습니다. 
프로세싱 이라는 프로그램도 써보았는데
이세상엔 정말 많은 다양한 프로그램이 있단걸 느꼈고 컴퓨터공학을 열심히 공부해 
심재창 교수님처럼 전문가가 되고 싶다고 생각 했습니다. 
아직은 아두이노를 이해하긴 쉽지 않지만 열심히 공부해서 좋은 성적 받을 수 있도록 노력 하겠습니다. 
다음 수업도 잘 부탁드립니다. 항상 학생들을 위해 노력해 주셔서 감사합니다. 사랑합니다 교수님♥

아두이노 코드

void setup()

{

  Serial.begin(9600);

}

int a;

void loop()

{

  a=analogRead(A0);

  Serial.println(++a);

  delay(500);

}

프로세싱 코드

import processing.serial.*;

Serial p;

void setup()

{

  size(300, 300);

  p=new Serial(this, "COM9", 9600);

}

void draw() {

  if (p.available()>0) {

  String m=p.readString();

  int a= int(m.trim());

  println(a);

  if(a>20) fill(0,255,0);

  else fill(255,0,0);

  ellipse(150,150,200,200);

  }

}
