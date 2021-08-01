# ConteudoProfundoTestes

<h1 align="center">
    <a href="https://www.youtube.com/watch?v=ZS66Nu7fNng">🔗 Aprendendo a testar direito #4: Boundary testing </a>
</h1>
<p align="center">🚀 Formulário de proposta de solução - Conteúdo mais profundo sobre testes 🚀 </p>

<h4 align="center"> 
	🚧  Orange Talents  🚀 Em construção...  🚧
</h4>


<p align="justify"> :robot: Descreva quais testes você faria para o método abaixo:robot: </p>


```
public boolean aceitaPalavra(String str){
  if(str == null || str.length() < 5){
     return false;
  }

  char primeiroCaractere = str.charAt(0);
  int tamanho = str.length();

 if (Character.isLetter(primeiroCaractere) 
        && (ultimoCaractere == 's' || tamanho >= 10)) {
        return true;
  } else {
    return false;
  }
}


```

### Minha resposta

<p align="justify"> :robot: Antes de iniciar vamos entender o fluxo do método aceitaPalavra, que recebe uma string “str” verificando no seu primeiro if se essa string é nula e possui um número inferior à 5 letras.
  
str.length ->  A propriedade length de um objeto String contém o comprimento da string. length é uma propriedade read-only (somente leitura) de instâncias de string.
  
str == null ->  Retorna verdadeiro caso os operandos sejam iguais.
  
Na segunda parte str.charAt(0) ele retorna o primeiro caractere de uma string guardando na variável primeiroCaractere e calcula o tamanho da variável “str”, guardando essa informação na variável tamanho.
  
Character.isLetter - > O método isLetter (char ch) da classe “Character” e determina se o caractere fornecido (ou especificado) é uma letra ou não.


No segundo “if” ele verifica de o primeiro caractere inserido na string “str” é uma letra “OU” se o último caractere possui o valor de “s” (ultimoCaractere == 's') e tem o tamanho menor que 10 caracteres (ultimoCaractere == 's' || tamanho >= 10).

:robot: </p>


<p align="justify"> :robot:
Pertinente destacar que o método apresenta falha uma vez que a variável ultimoCaractere não é declarada nem iniciada no método. Então possivelmente o “especialista” se esqueceu de implementar a coleta dessa informação que poderia ser feita assim: 
char ultimoCaractere = str.charAt(str.length() - 1);
  
Agora com essas informações vou iniciar a testagem com o primeiro “if” passando:
  
Referente o primeiro if:
- [x] O “in point” de 5 caracteres, ou seja o valor exato de valor que define a condição;
- [x] O	“off point” de 6 caracteres que passa o valor de condição;
- [x] O “in point” de 4 caracteres para verificar valores equivalentes inferiores a 5.
  
Referente o segundo if:
- [x] O “in point” de 10 caracteres, ou seja o valor exato de valor que define a condição;
- [x] O “off point” de 11 caracteres que passa o valor de condição;
- [x] O “in point” de 9 caracteres para verificar valores equivalentes inferiores a 10.
  
- [x] Realizar um teste com uma string nula;
  
- [x] Realizar dois testes com 10 e 9 caracteres ambas terminam com a letra “s”.

:robot: </p>
