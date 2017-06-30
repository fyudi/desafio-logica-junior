Desafio de lógica
============

Esta página contém as informações referentes ao desafio de lógica para desenvolvedores juniors / assistentes

### Código de honra

Ao realizar esse desafio, você se compromete a:

* Não consultar outras pessoas sobre estratégias e soluções para os problemas propostos
* Não consultar mecanismos de busca online e offline sobre estratégias e soluções para os problemas propostos

### Questões


1. Você tem 8 moedas e todas tem o mesmo peso exceto uma, que é um pouco mais pesada que as demais. Você também possui uma balança que permite pesar duas pilhas de moedas para descobrir qual é a mais pesada (ou de mesmo peso). Qual é o mínimo número de combinações para serem feitas para descobrir qual a moeda mais pesada?
```
Total de pesagens em todos os três casos abaixo: 2

caso1:
-Pesar três moedas de um lado e três moedas do outro (pesagem 1) se a balança ficar equilibrada então pesar as duas moedas restantes (pesagem 2), o lado da balança que estiver mais pesado é o que possui a moeda mais pesada.

caso2:
-Pesar três moedas de um lado e três moedas do outro (pesagem 1) se a balança não ficar equilibrada, prosseguir pesando duas das três moedas do lado mais pesado, sendo uma em cada lado da balança (pesagem2). O lado da balança que estiver mais pesado é o que possui a moeda mais pesada.

caso3:
-Pesar três moedas de um lado e três moedas do outro (pesagem 1) se a balança não ficar equilibrada, prosseguir pesando duas das três moedas do lado mais pesado, sendo uma em cada lado da balança (pesagem2). Se os dois lados permanecem equilibrados é porque a moeda que ficou de fora da pesagem é a moeda mais pesada.

```

2. Assuma um cubo semelhante ao do desenho abaixo, no entanto com 8 mini cubos em cada aresta. Se pintarmos todas as suas faces, quantos mini cubos terão pelo menos uma face pintada?

![alt text] (https://raw.githubusercontent.com/maplink/desafio-logica-junior/master/121016-4x4x4-cube-175w.gif "Cubo 4x4")

```
//para cada face
8 * 8 = 64

//total de lados de um cubo
6 * 64 = 

//subtraindo faces repetidas
384 - 64 = 320    

total = 320
```

3. Dado um array de inteiros ordenados, como encontrar a posição de determinado valor?


```javascript
//Using JavaScript

function returnPosition (array, value) {
  
  if (array.indexOf(value) != -1 ){
    return array.indexOf(value);
  }
   //When the number is not found by indexOf -1 is returned, so return 'false'
  return false; 
}

//Testing
window.alert(returnPosition([0,1,2,3,4,5,6,7,8], 6));
```


4. Escreva um código para reverter uma string.

```javascript
//Using JavaScript to invert a specific word

function reverseWord (word) {

  var newWord = "";

	for (var i = word.length; i >= 0 ; i--){

	  newWord = newWord + word.substr(i, 1);
	}
	return newWord;
}

//Testing
window.alert(reverseWord("MARROCOS"));
```

```sql
--PL/SQL
set serveroutput on
declare
  word varchar2(4000)     := 'MARROCOS';
  new_word varchar2(4000) := null;
  qtd number              := null;
begin
  qtd := length(word);

  for i in reverse 0..qtd 
  loop
    new_word := new_word || substr(word, i, 1);
  end loop;
   dbms_output.put_line(new_word);
end;

```


### Envio da solução

Você pode realizar a implementação dos código na linguagem de programação de sua preferência. Use sua criatividade! 

O compartilhamento do resultado produzido deve ser feito diretamente pelo GitHub. Para isso, faça um <a href="https://help.github.com/articles/fork-a-repo" target="_blank">fork</a> e nos envie sua versão com a devida implementação e incluindo seus nome completo.

Qualquer dúvida, você pode enviar um e-mail para rhti@maplink.com.br.

Bom desafio!

*Time Maplink*





