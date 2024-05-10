# Desafio DIO - Implementação de Validações de Testes Unitários com C#



O objetivo deste projeto é implementar validações de testes unitários em um aplicativo C# para garantir que o código esteja funcionando conforme o esperado. Os testes unitários são uma técnica de teste de software que testa unidades individuais de código, como funções ou classes. Ao implementar validações de testes unitários, os desenvolvedores podem identificar e corrigir erros no código em um estágio inicial, o que ajuda a prevenir bugs e melhorar a qualidade geral do software.



## **Requisitos:**

- O projeto deve implementar validações de testes unitários em um aplicativo C#.
- Os testes unitários devem testar unidades individuais de código, como funções ou classes.
- As validações de teste devem verificar se o código está funcionando conforme o esperado.

## Resultado do Projeto
<img>

## Tecnologias Utilizadas

| Linguagens de Programação | Ferramentas e Tecnologias |
| :-----------------: | :-----------------------: |
| <img height="40" src="https://github.com/rhayssakramer/rhayssakramer/blob/main/assets/icon/C%23.svg"> <img height="40" src="https://github.com/rhayssakramer/rhayssakramer/blob/main/assets/icon/dotnet.svg"> <img height="40" src="https://github.com/rhayssakramer/rhayssakramer/blob/main/assets/icon/NodeJS-Dark.svg"> | <img height="40" src="https://github.com/rhayssakramer/rhayssakramer/blob/main/assets/icon/VSCode-Dark.svg">



## **Regras de negócio:**

- As validações de teste unitário devem ser implementadas para todas as unidades de código críticas.
- As validações de teste unitário devem ser executadas automaticamente como parte do processo de construção.



## Requisitos do Projeto

#### Projeto - Console

- Desafio de projeto: Para este desafio, foi preciso usar os conhecimentos adquiridos no módulo de Testes Unitários com C#, da trilha .NET da DIO.

- Contexto: Na proposta desafio o desenvoledor está trabalhando em um sistema, e seus gestores relataram que frequentemente há problemas no software: bugs, funcionalidades que estavam funcionando de repente não funcionam mais, problemas de validações, entre outros. Os clientes já começam a duvidar da qualidade do código. Feito isso, foi sugerido a implementação de testes unitários: escrever testes cobrindo as partes mais críticas do sistema, com cenários positivos e negativos, a fim de ter uma rastreabilidade e controle do código, melhorando assim a qualidade desse sistema. Os gestores aceitaram a sua ideia, e com isso, foi preciso implementar testes unitários no sistema.

- Premissas: O sistema hoje possui dois projetos: um do tipo console, e um do tipo testes com xUnit. O projeto do tipo console possui duas classes em que são realizadas as lógicas principais: ValidacoesLista e ValidacoesString. Essas classes contém métodos em comum que são usados para realizar diversas validações em determinados cenários. O projeto de testes possui as classes de teste ValidacoesListaTests e ValidacoesStringTests, assim como seus métodos para validar o projeto do tipo console, porém estão incompletos. O meu objetivo foi implementar os métodos de testes contidos no projeto.

- Estrutura do projeto: O projeto está estruturado da seguinte maneira:

<img width="220" src="">



### Projeto Console, suas classes e métodos

Essas são as classes do projeto console, onde fica a principal lógica do sistema.

**Classe ValidaçõesLista:** classe responsável por realizar diversas validações envolvendo listas.

| Classe          | Método                       | Objetivo                                                                                                                |
|---------------- |------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ValidacoesLista | RemoverNumerosNegativos      | Recebe uma lista de números inteiros e retorna uma nova lista, apenas com os números positivos                          |
| ValidacoesLista | ListaContemDeterminadoNumero | Recebe uma lista de números inteiros e verifica se um determinado número está presente dentro dessa lista               |
| ValidacoesLista | MultiplicarNumerosLista      | Recebe uma lista de números inteiros e retorna uma nova lista, com seus valores múltiplicados por um determinado número |
| ValidacoesLista | RetornarMaiorNumeroLista     | Recebe uma lista de números inteiros e retorna o maior número entre eles                                                |
| ValidacoesLista | RetornarMenorNumeroLista     | Recebe uma lista de números inteiros e retorna o menor número entre eles                                                |

**Classe ValidacoesString:** classe responsável por realizar diversas validações envolvendo strings.

| Classe           | Método                       | Objetivo                                                                                                                
|------------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesString | RetornarQuantidadeCaracteres | Recebe um texto qualquer e retorna a quantidade de caracteres presentes no texto                                                                           |
| ValidacoesString | ContemCaractere              | Recebe um texto qualquer e um texto a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no texto                 |
| ValidacoesString | TextoTerminaCom              | Recebe um texto qualquer e um trecho a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no final do texto apenas |



### Projeto do tipo teste, suas classes e métodos

**Classe ValidacoesListaTests:** classe responsável por realizar os testes da classe ValidacoesLista.

| Classe               | Método de teste                               | Resultado esperado do teste
|----------------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesListaTests | DeveRemoverNumerosNegativosDeUmaLista         | Ao passar uma lista com diversos números, incluindo positivos e negativos, deve ser retornado uma nova lista apenas com números positivos  |
| ValidacoesListaTests | DeveConterONumero9NaLista                     | Ao passar uma lista com diversos números, incluindo o número 9, deve retornar verdadeiro, pois encontrou o 9 na lista                      |
| ValidacoesListaTests | NaoDeveConterONumero10NaLista                 | Ao passar uma lista com diversos números, mas sem o número 10, deve retornar falso, pois não encontrou o 10 na lista                       |
| ValidacoesListaTests | DeveMultiplicarOsElementosDaListaPor2         | Ao passar uma lista de inteiros, deve retornar uma nova lista, com todos os elementos da lista multiplicados por 2                         |
| ValidacoesListaTests | DeveRetornar9ComoMaiorNumeroDaLista           | Ao passar uma lista de números inteiros, sendo o maior deles 9, deve retornar o 9 como maior elemento dentro dessa lista                   |
| ValidacoesListaTests | DeveRetornarOitoNegativoComoMenorNumeroDaList | Ao passar uma lista de números inteiros, sendo o menor deles -8, deve retornar o -8 como menor elemento dentro dessa lista                 |



**Classe ValidacoesStringTests:** classe responsável por realizar os testes da classe ValidacoesString.

| Classe                | Método de teste                                  | Resultado esperado do teste
|---------------------- |--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesStringTests | DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | Ao passar um texto escrito a palavra "Matrix", deve retornar o número 6, representando 6 caracteres presentes na palavra                                                                         |
| ValidacoesStringTests | DeveContemAPalavraQualquerNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "qualquer", deve retornar verdadeiro pois a palavra existe no texto                                                |
| ValidacoesStringTests | NaoDeveConterAPalavraTesteNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "teste", deve retornar falso pois a palavra não existe no texto                                                    |
| ValidacoesStringTests | TextoDeveTerminarComAPalavraProcurado            | Ao passar um texto escrito "Começo, meio e fim do texto procurado" e procurar pela palavra "procurado", deve retornar verdadeiro pois a palavra existe no texto e está inclusa no final do texto |



## **Aprendizado e Aplicabilidade Prática**

- Os testes unitários são uma técnica valiosa para melhorar a qualidade do software.
- Os testes unitários podem ajudar a identificar e corrigir erros no código em um estágio inicial.
- Os testes unitários podem ser automatizados como parte do processo de construção, garantindo que o código seja testado regularmente.
- Os testes unitários podem ser aplicados a qualquer aplicativo C# para melhorar sua qualidade e confiabilidade.



## Solução

O código de testes está pela metade, e você deverá dar continuidade implementando os testes descritos acima, para que no final, tenhamos um programa de testes funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.



## Instruções de Uso

1. Clone ou baixe este repositório para a sua máquina local.

2. Certifique-se de ter o [Node.js](https://nodejs.org/en/download/current) e [.NET 8.0](https://dotnet.microsoft.com/pt-br/download) instalado em sua máquina.

3. Abra o terminal e navegue até o diretório raiz do projeto.

4. Para corrigir os erros, utilize o comando:
```
dotnet build
```

5. Para executar o teste, utilize o comando:
```
dotnet test
```



## **Conclusão**

Implementar validações de testes unitários em um aplicativo C# é uma prática essencial para garantir a qualidade e confiabilidade do código. Os testes unitários ajudam a identificar e corrigir erros no código em um estágio inicial, o que pode economizar tempo e esforço no longo prazo. Ao implementar validações de testes unitários, os desenvolvedores podem garantir que seu código esteja funcionando conforme o esperado e atender aos requisitos do projeto.



## **Aprendizado e Aplicabilidade Prática**

- Os testes unitários são uma técnica valiosa para melhorar a qualidade do software.
- Os testes unitários podem ajudar a identificar e corrigir erros no código em um estágio inicial.
- Os testes unitários podem ser automatizados como parte do processo de construção, garantindo que o código seja testado regularmente.
- Os testes unitários podem ser aplicados a qualquer aplicativo C# para melhorar sua qualidade e confiabilidade.





Agradecimento: 

<table>
  <tr>
    <td>
      <img width="80px" align="center" src="https://github.com/rhayssakramer/rhayssakramer/blob/main/assets/images/logo.png"/>
    </td>
    <td align="left">
      <a href="https://github.com/rhayssakramer">
        <span><b>Rhayssa Kramer</b></span>
      </a>
      <br>
      <span>Desenvolvedora Full Stack</span>
    </td>
  </tr>
</table>

