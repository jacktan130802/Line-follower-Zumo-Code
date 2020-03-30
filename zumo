 int turn_delay = 40;
   


  const int rightMotor =7 ;
  const int leftMotor= 8 ;
  const int rightSpeed =9;
  const int leftSpeed =10;

//Sensor Connection
  const int left_sensor_pin = A2;
  const int right_sensor_pin = A0;

  
  
  int left_sensor_state;
  int right_sensor_state;

void setup() {
  pinMode(rightMotor, OUTPUT);
  pinMode(leftMotor, OUTPUT);
  pinMode(rightSpeed, OUTPUT);
  pinMode(leftSpeed, OUTPUT);
  pinMode(left_sensor_pin,INPUT_PULLUP);
  pinMode(right_sensor_pin,INPUT_PULLUP);

  Serial.begin(9600);

  delay(3000);
  
}

void loop() {
  

  


left_sensor_state = analogRead(left_sensor_pin);
right_sensor_state = analogRead(right_sensor_pin);

if(right_sensor_state > 500 && left_sensor_state < 500)//when turning can try of thinking marching to the left and how it goona change
{
  Serial.println("turning right");//RIGHT WHITE,LEFT BLACK

  digitalWrite (rightMotor,LOW);
  digitalWrite(leftMotor,LOW);                       


  analogWrite (rightSpeed,220);
  analogWrite (leftSpeed,1);
  delay(turn_delay);
  }
if(right_sensor_state < 500 && left_sensor_state > 500) //RIGHT black,LEFT white
{
  Serial.println("turning left");
  
  digitalWrite (rightMotor,LOW);
  digitalWrite(leftMotor,LOW);                       



  analogWrite (rightSpeed,1);
  analogWrite (leftSpeed,220);

  delay(turn_delay);
  }

if(right_sensor_state > 500 && left_sensor_state > 500)
{
  Serial.println("going forward");

  digitalWrite (rightMotor,LOW);
  digitalWrite(leftMotor,LOW);                       

  analogWrite (rightSpeed,50);
  analogWrite (leftSpeed,50 );

  

  delay(turn_delay);
  }

if(right_sensor_state < 500 && left_sensor_state < 500)
{ 
  Serial.println("stop");
  
  analogWrite (rightSpeed,0);
  analogWrite (leftSpeed,0 );

  
  }

 
}
