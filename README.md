### Cds-조도센서

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
  
