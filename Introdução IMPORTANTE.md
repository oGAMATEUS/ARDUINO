// as duas barras sao usadas para fazer comentarios no meio do codigo, ou seja uma linha que nao é lida pelo computador 
/* esta é a outra maneira de fazer uma comentario no entanto essa nao é apenas para a linha e sim para o começo e o fim do esterisco com barra */


int var-nome = 9; // introduzindo o nome de uma variavel e se atual valor 
int estado_sensor = 0; // introduzindo o nome de uma variavel e se atual valor 
 
void setup()
{
  Serial.begin(9600);
  // Define o pino do sensor como entrada
  pinMode(pino_sensor, INPUT);
  
  Serial.println("Teste sensor infravermelho Arduino");
}
 
void loop()
{
  estado_sensor = digitalRead(pino_sensor);
  if (estado_sensor == 0)
  {
    // com objeto na frente do sensor, ele escreve 
    Serial.println("tem algo aqui");
    delay(1000);
  }
  else
  {
    // Sem OBJETO, escreve a seguinte mensagem 
    Serial.println("lonely");
  }
}
