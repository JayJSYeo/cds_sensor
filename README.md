***Cds-조도센서***
----------------



### 조도 센서에 대해 알아보기 링크
  
[기초 배우기]:https://m.blog.naver.com/PostView.nhn?blogId=dokkosam&logNo=221168232261&proxyReferer=https%3A%2F%2Fwww.google.com%2F
[기초 배우기]


<img src="https://github.com/JayJSYeo/cds_sensor/blob/master/25779848587C70B121.jpg" width="25%">

조도 센서는 빛을 측정하는데 그것을 이용해 브레드 보드중간에 종이를 꽂아 놓고 조도센서를 양쪽에 두어 빛의 세기를 측정해 빛이 어느쪽으로부터 들어 오는지 알아냈다(시리얼 모니터).

```cpp
void setup() {
  // put your setup code here, to run once:

  Serial.begin (9600);

}

void loop() {
  // put your main code here, to run repeatedly:

  int valueleft ;
  int valueright ;
  int difference;
  
  valueleft = analogRead(A0) ;
  valueright = analogRead(A1) ;

  //Serial.println(valueleft) ;
  //Serial.println(valueright) ;

  difference=valueleft-valueright;
  //Serial.println(difference);

 
  if( difference <-30 ){
    Serial.println("left");
  }else if( difference<30){
    Serial.println("center") ;
  }else{
    Serial.println("right") ;
  }
  
 
   delay(500) ;

  

}
```
  
