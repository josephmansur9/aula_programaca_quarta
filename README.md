# aula_programaca_quarta




[foto do circuito](foto.png)




```C++
class LED {
  #so pode ser usado na clase
  private:
  #qual pino
    int pin;
```
Essa parte cria a classe led, o private faz com que esse codígo so pode ser usado nessa classe. O int pin vai guardar o numero do pino em um numero inteiro.

```C++
 #vai ser usado fora da classe
  public:
  #roda quando voce cria um led, entao qual vai ser o pino é o int p
    LED(int p) {
      #salva a variavel
      pin = p;
      #output
      pinMode(pin, OUTPUT);
    }
```
public significa que pode ser usado fora da calasse, o led roda quando voce cria um led por ser um consrtuctor. O int recebe o numero do pino, depois dalva o p como a variavel pino, e seta o pino como um output.


```C++
    #servve pra ligar
    void on() {
      #manda o sinal high
      digitalWrite(pin, HIGH);
    }
```
serve pra ligar o led, ou seja manda o sinal HIGH pro led

```C++ 
    #serve pra desligar
    void off() {
      #manda o sinal low
      digitalWrite(pin, LOW);
    }
};
```
faz o mesmo mas para desligar


```C++
LED redLED(10);
LED greenLED(12);
LED yellowLED(13);

```
define as saidas dos leds

```C++
void setup() {
}
```
funcao

```C++ 
void loop() {
  redLED.on();
  greenLED.off();
  yellowLED.off();
  whiteLED.off();
  delay(500);
  
  redLED.off();
  greenLED.on();
  yellowLED.off();
  whiteLED.off();
  delay(500);
  
  redLED.off();
  greenLED.off();
  yellowLED.on();
  whiteLED.off();
  delay(500);
  
  redLED.off();
  greenLED.off();
  yellowLED.off();
  whiteLED.on();
  delay(500);
  
  delay(500);

```
cria um loop, onde quando liga um led, o outro deslgia, depois liga o outro led, e os outros dois desligam, eu poderia adicionar mais leds, ate acabar as entradas.

