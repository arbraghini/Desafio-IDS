# Desafio-IDS
Programa de seleção da Empresa IDS
DESAFIO 01
// Programa para calcular a pontuação de uma palavra digitada pelo usuário, através de uma tabela de valores //

======================================================================================================================

Passos para executar o programa em Java.
 1 - Salve o arquivo o programa em alguma Pasta do Windows.
 2 - Clique no botão Iniciar e digite cmd. Pressione ↵ Enter para abrir o "Prompt de Comando".
 3 - Verifique se o Java está instalado. Digite java -version na linha de comando. Se o Java estiver instalado, você verá uma mensagem mostrando qual a versão dele          está instalada. Se isso não acontecer, será necessário acessar o site do Java e baixar o Java Development Kit (JDK), que é gratuito e pode ser encontrado aqui:        http://www.oracle.com/technetwork/java/javase/downloads/index.html.
 4 - Vá até a pasta correta. Use o comando cd seguido pelo nome da pasta de destino para sair do diretório atual.
     Por exemplo, se você estiver no diretório C:\Users\Bob\Project e quiser acessar a pasta C:\Users\Bob\Project\TitanProject , digite cd TitanProject e pressione ↵        Enter. Para mostrar uma lista com todos os arquivos e pastas do diretório atual, digite dir no Windows ou ls no Mac e pressione ↵ Enter
 5 - Execute o programa. Digite java arquivo e pressione ↵ Enter. Lembre-se de que você deve trocar "arquivo" pelo nome do arquivo do seu programa.
     Após pressionar ↵ Enter, o programa deve rodar.
 
 
 
 
 
import java.util.Scanner;

public class PontuacaoPalavra

{ public static void main( String args[ ])
	{
	int pontuacao = 0;
	String palavra;
	Scanner p = new Scanner(System.in);
	System.out.println("Digite uma palavra: ");
	palavra = p.next();
	palavra = palavra.trim();
	palavra = palavra.toUpperCase();
	String listaum = "A E I O U L N R S T";
	String listadois = "D G";
	String listatres = "B C M P";
	String listaquatro = "F H V W Y";
	String listacinco = "K";
	String listaseis = "J X";
	String listasete = "Q Z";
	for (int n=0; n < palavra.length(); n++){
		if (listaum.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 1;
		if (listadois.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 2;
		if (listatres.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 3;
		if (listaquatro.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 4;
		if (listacinco.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 5;
		if (listaseis.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 8;
		if (listasete.contains(String.valueOf(palavra.charAt(n))))
		pontuacao = pontuacao + 10;
 		}
System.out.println(" A pontuacao da Palavra "+ palavra + " = " + pontuacao );
	}
}
