# ChatBot Java

## Objetivo  

O objetivo do software é ser uma especie de chat-bot, programado na linguagem **java** que responde a certas perguntas.

## Funcionamento  

#### Perguntas e respostas  

O chat bot funciona com palavras-chave, então, caso o usuário digite algo com a palavra **nome**, o chat bot retornará seu nome

![Pergunta Nome CHATBOT](https://github.com/pauloszuparits/Imagens/blob/d9ba44d6c2f280e418382247fcd0b9140ed02426/imgChatBot/NomeCHATBOT.png)

Digitando a palavra **dia** o chat bot retornará que dia é hoje  

![Pergunta dia CHATBOT](https://github.com/pauloszuparits/Imagens/blob/d9ba44d6c2f280e418382247fcd0b9140ed02426/imgChatBot/DiaCHATBOT.png)  

Digitando **horas** o chat bot retornará a hora atual  

![Pergunta horas CHATBOT](https://github.com/pauloszuparits/Imagens/blob/d9ba44d6c2f280e418382247fcd0b9140ed02426/imgChatBot/HoraCHATBOT.png)  

Digitando **contar** o chat abre uma contagem e à incrementa toda vez que digitar **contar**  

![Pedir para contar CHATBOT](https://github.com/pauloszuparits/Imagens/blob/d9ba44d6c2f280e418382247fcd0b9140ed02426/imgChatBot/ContarCHATBOT.png)  

Por fim, você pode pedir para o chat-bot contar uma **piada** para você, ele possui algumas piadas no banco de dados e escolherá uma de forma aleatória  

![Pedir piada CHATBOT](https://github.com/pauloszuparits/Imagens/blob/d9ba44d6c2f280e418382247fcd0b9140ed02426/imgChatBot/PiadaCHATBOT.png)  

## Documentação técnica  

### Classes  

#### Resposta

A classe Resposta é uma classe abstrata que possue 2 métodos, o verifica e o produz.

![Classe Resposta](https://github.com/pauloszuparits/Imagens/blob/662347d59bf755cac0ad7fce751922589c969028/DocTecnicaChatBot/classeResposta.png)

#### ChatBot  

A classe ChatBot tem 2 parametros, sendo eles:  
- String[] stringCortada;
- ArrayList<Resposta> respostasAleatorias;  

E possui 1 construtor que inicia um ArrayList.  

##### Métodos  

A classe ChatBot possui 2 métodos:
- adciona -> recebe uma Resposta e a adiciona no arrayList  
- processar -> recebe uma String e chama a funcao verifica da classe Respostas aleatórias, caso vericia retorne um true, retorna uma respota, se não, retorna uma string vazia  

![Classe ChatBot](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeChatBot.png)  

#### RespostaAleatoria  

A classe respostaAleatoria herda da classe Resposta e possui 2 parametros, sendo eles:
- String entradaUser;
- ArrayList<String> respostasAleatorias;  

E possui um construtor, que recebe uma String, e um ArrayList<String>  

##### Métodos  

A classe RespostaAleatoria possue 2 métodos herdados da classe Resposta:  
- verifica -> recebe uma string e retorna um boolean  
- produz -> pega uma resposta aleatóriamente do ArrayList e retorna.  

![classe RespostaAleatoria](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeRespostaAleatoria.png)  
  
#### RespostaSimples  

A classe RespostaSimples possue 2 parametros, sendo eles:  
- final String resposta;
- final String entradaUser;  

E possue um construtor que recebe duas String  

##### Métodos  

A classe RespostaSimples possue dois métodos herdados de Resposta, o verifica e o produz. 

![Classe Resposta Simples](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeRespostaSimples.png)  
  
#### RespostaContador  
  
a classe RespostaContador contador possue 2 parametros, sendo eles: 
- String entradaUser;
- int cont;  
  
E possue um construtor que recebe uma string.  
  
##### Métodos  
  
A classe RespostaContador possue dois métodos herdados de Resposta, o verifica e o produz.  
  
![Classe RespostaContador](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeRepostaContador.png)  
  
#### RespostaHora

A classe RespostaHora possue 3 parametros, sendo eles:  
  
- int hora;
- int minuto;
- String entradaUser;  
  
E um construtor, que recebe um String.  

##### Métodos  
  
A classe RespostaHora possue 2 métodos que herdam da classe Resposta, o verifica e o produz.  

![Classe RespostaHora](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeRespostaHora.png)  
  
#### RespostaData  
  
A classe RespostaData possue 4 parametros, sendo eles:  
  
- String entradaUser;
- int dia;
- int mes;
- int ano;
  
E possue um construtor que recebe uma string.  
  
##### Métodos  
  
A classe RespostaData possue 2 métodos que herdam da classe Resposta, o verifica e o produz.  
  
![Classe RespostaData](https://github.com/pauloszuparits/Imagens/blob/4e2b4d8bd0de6843f00fd7eca1a38cee703a251a/DocTecnicaChatBot/classeRespostaData.png)
  



 
