![senai_logo](https://transparencia.sp.senai.br/Content/img/logo-senai.png)

# Lista de Exercícios 01: Fluxogramas

Profº.: Cainã Antunes Silva  
Faculdade de Tecnologia **SENAI Sorocaba**  
Tecnólogo em Análise e Desenvolvimento de Sistemas (ADS)
___


> O objetivo desta aula é exercitar o raciocínio lógico para a criação de algoritmos através de fluxogramas.  

O fluxo de um algorítmo poder ser representado graficamente através de fluxogramas. Um conjunto de símbolos, representam cada ação realizada pelo programa, além disso, setas conectam estes símbolos uns com os outros indicando a sequencia em que as ações são executadas.

Para mais informações acesse [Aula 01: Fluxogramas.](https://www.notion.so/cainaantunes/Aula-01-Fluxogramas-188bde521b3b80de90f7dbd9407af71e)

***

1. Crie o fluxograma de um programa que solicita que o usuário digite sua nota e em seguida o programa exibe se o aluno foi “Aprovado” ou “Reprovado”. Leve em consideração que a nota deve estar entre 0 e 100 e que a condição para aprovação é ter uma nota igual ou superior à 50.
   
    ```mermaid
   
    flowchart TD
        start(( Início )) --> input[\ Digite sua Nota \]
        input --> verification{ Nota >= 50? }
        verification --> |Sim| A[/ Aprovado /]
        verification --> |Não| B[/ Reprovado /]
        A --> finish([ Fim ])
        B --> finish
    ```
   
2. Altere o exemplo anterior, acrescentando as seguintes condições: para ser o aprovado, o aluno precisar ter nota igual ou superior à 50 e frequência igual ou superior a 75%.
   
   ```mermaid
   flowchart TD
      start((Inicio))-->input1[\digite sua nota - valor entre 0 e 100\]
      input1-->input2[\digite sua frequencia em %\]
      input2-->verification{Nota >=50 /n E /n Frequencia >=75}
      verification--> |sim| A[/Aprovado/]
      verification--> |Não| B[/Reprovado/]
      A-->finish([Fim])
      B-->finish
   ```
   
3. Crie um fluxograma para calcular a soma de dois números fornecidos pelo usuário.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input1[\digite número1\]
      input1-->input2[\digite número2\]
      input2-->soma[resultado=numero1+numero2]
      soma-->resultado[/resultado/]
      resultado-->finish([fim])
   ```
   
4. Elabore um fluxograma que leia um número e exiba se ele é positivo ou negativo.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input1[\digite um número\]
      input1-->verification{N>=0}
      verification-->|sim| A[/Positivo/]
      verification-->|não| B[/Negativo/]
      A-->finish([Fim])
      B-->finish
   ```
   
5. Desenvolva um fluxograma que leia a idade de uma pessoa e indique se ela pode votar.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input1[\digite sua idade\]
      input1-->input2[\digite S se possui título\]
      input2-->verification{idade >=16 E possui título}
      verification-->|sim|A[/Pode votar/]
      verification-->|não|B[/Não pode votar/]
      A-->finish(Fim)
      B-->finish
   ```
   
6. Crie um fluxograma que leia dois números e determine o maior entre eles.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input1[\digite N1\]
      input1-->input2[\digite N2\]
      input2-->Resultado{identificar N1>=N2}
      Resultado-->|sim|A[/N1/]
      Resultado-->|não|B[/N2/]
      A-->finish(Fim)
      B-->finish
   ```
   
7. Crie um fluxograma que leia três números e determine o maior entre eles.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input1[\digita N1\]
      input1-->input2[\digite N2\]
      input2-->input3[\digite N3\]
      input3-->Resultado1{N1>N2}
      Resultado1-->|sim|A{N1>N3}
      Resultado1-->|não|B{N2>N3}
      A-->|sim|C[/N1 é o maior/]
      A-->|não|D
      B-->|não|D{N3==N1 OR N3==N2}
      B-->|sim|J[/N2 é maior/]
      D-->|sim|H[/Você digitou \n alguns números \n iguais/]
      D-->|não|I[/N3 é o maior/]
      C-->finish(fim)
      H-->finish
      I-->finish
      J-->finish
   ```
   
8. Construa um fluxograma para calcular o fatorial de um número fornecido pelo usuário.
   
   ```mermaid
   flowchart TD
      start((inicio))-->input[\Digite um número\]
      input-->a[r=1]
      a-->b{n>1?}
      b-->|sim|c[r=r*n]
      c-->d[n=n-1]
      d-->b
      b-->|não|e[/resposta = r/]
      e-->finish(final)
   
   ```
   
9. Elabore um fluxograma para verificar se um número digitado pelo usuário é par.
   
   > Em várias linguagens de programação, o operador % retorna o resto da divisão entre dois números.    
   > 
   >**Exemplos**:  
   > - 9 % 2 = 1  
   > - 11 % 3 = 2
   
   ```mermaid
   flowchart TD
      start((inicio))-->B[\digite um número\]
      B-->C{N%2==0?}
      C-->|sim|d[/par/]
      C-->|não|e[/impar/]
      d-->finish(fim)
      e-->finish
   ```
   
10. Elabore um fluxograma para verificar se um número digitado pelo usuário é primo.
   
   ```mermaid
   flowchart TD
      I["Sua resposta aqui!"]
   ```