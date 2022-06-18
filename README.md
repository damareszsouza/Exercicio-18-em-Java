# Exercicio-18-em-Java
ATRIBUTOS PRIVATE, MÉTODOS PUBLIC- Replicado do Livro Tutorial Java

ATRIBUTOS PRIVATE, MÉTODOS PUBLIC
Aplicando encapsulamento a classe ponto definida anteriormente, deixando os atributos
encapsulados e definindo a interface publica da classe somente através de métodos.
//Classe ponto
public class Ponto {
private float x,y; //atributos private
public Ponto(float ax,float ay) //omita o valor de retorno!
//garante o estado do objeto
{
 this.x=ax; this.y=ay;
}
public void move(float dx,float dy)
{
 this.x+=dx; this.y+=dy;
 }
public float retorna_x()
{
return x;
}
public void mostra()
{
System.out.println( "(" + this.x + "," + this.y + ")" );
}
}
//Classe principal, Arquivo Principal.java
class Principal {
 public static void main(String args[]) {
 Ponto ap;
 ap=new Ponto((float)0.0,(float)0.0);
 ap.mostra();
 }
}
(0,0)

//COMENTARIOS: 
Este programa não deixa você tirar o ponto de (0,0) a não ser que seja chamada inicializa
novamente. Fica claro que agora, encapsulando x e y precisamos de mais métodos para que a classe
não tenha sua funcionalidade limitada. Novamente: escrever ap.x=10; em main é um erro! Pois x
está qualificada como private. Sempre leia os exercícios, mesmo que não vá faze-los. O que ocorre
em classes mais complicadas, é que ao definir mais métodos na interface da classe, estamos
permitindo que a representação interna possa ser mudada sem que os usuários tomem conhecimento
disto.
