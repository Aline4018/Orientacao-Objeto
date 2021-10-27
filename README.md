Orientação a Objeto em TS
=============
#### 4 Pilares de Orientação Objeto
 + Abstração
 > => Transforma o nosso problema do mundo real o mais próximo possível da programação
- 1 Identidade = Produto
- 2 Atributos = Nome, Quant. em estoque …
- 3 Métodos e ações = Dar baixa em estoque ...

+ Encapsulamento
> => Protege as aplicações ...

+  Herança
> => Reutilizar código
+ Polimorfismo
>=> 	Dinamismo para trabalhar chamadas com comportamentos diferentes debaixo dos panos.

#### Vantagens
+ => Prática de programação
Representação do mundo real
+ => Segurança
Facilitadores Colocar dentro do meu projeto como proteção de campo.
+ => Reutilização de código
Herança e Polimorfismo, ganha isso muito forte.
+ => Fácil manutenção
Consigo ir com facilidade nos pontos.

#### A Estrutura
- Classe: 
Abstração do que há em comum ( em termos de características e comportamentos) à um conjunto de objetos.

> Classe
- Atributos
características
- Métodos
comportamentos 

#### Exemplo 1 :
- Escolha pontos em comum em um objeto e fazer à classe que engloba todos.

 > Classe:
- Mamífero 

 > Atributos
- Carct. comum nos mamíferos
 + Data de nascimento
 + Peso
 + Energia
 + Métodos
> Ações 

    - Comer
    - Mover
    - Mamar
	
#### Exemplo 2:
 > Classe:
-  Empresa (Objeto)

  +  Esqueleto: 
 > Atributos
- Carct. comum nas empresas
 + Nome
 + Cnpj
 + Funcionários [ ]

  
  > Métodos (Ações) 
   - Contratar
   - Demitir

     Funcionário
 - (Atributos)
  + Nome
  + CPF
  + Salário

- (Métodos)
   + Trabalhar
   + Fofocar
   + Bater ponto
     ####Objeto (2/2)
- Objetos servem como uma base real para a elaboração de um sistema consistente com a realidade modelada.
Ex. Um livro, um telefone, uma faculdade, um produto, um aluno, um professor.

                  Classe e Objeto (½)
- Classe é o que projetamos
-  Objeto é o que criamos a partir da classe
-  As classes estão para os objetos assim como as plantas arquitetônicas estão para as casas

        Classe e Objeto (2/2) - Montar o Esqueleto

| Carro     | 
| --------- | 
| Marca | 
| Modelo     |  
| Ano      | 
| Potencia    | 

| Metodo ( Ações )
| :------------ |
| Acelerar    |
| TrocarMarcha    | 

#### TyperScript :
- Tem o intuito de ajudar em vários pontos e ajuda na orientação Objeto;
- Códigos mais elegantes e utilizados;
- Intellisense e verbosidade: Autocompile, opções para manipulação da string, feedbacks em tempo de compilação, recursos mais completos do Javascript, produtividade, Tipagem.

#### Encapsulamento
- Criamos a classe personagem, definimos atributos para ela, Deixamos todos eles com o Public que é um modificador de acesso. Deixamos os menbros da nossa classe expostos. Os metodos estão expostos do nosso objeto.
-  Passar a proteger os atributos e prover acessos de forma moderada para para eles. Prooteger da nossa classe tudo que noso temos.
-  A proposta de isolar o maximo possivel as classes, de forma a esconder detalhes de funcionamento interno.
-  Visa aumentar a flexibilidade, melhorar a manutençaõ e aumentar a extensibilidade do software.
- Modificadores de acesso: Permitem configurar a visibilidade dos nossos atributos, classes e metodos.
#### Modificadores de acesso
- Public  (+)
- Utilizada de forma restrita, apenas quando desejamos que outras classes " Enxerguem" nossa classe, metodo ou atributo. Torna visivel em todo o projeto.
- Metodos, sempre que possivel não devem ser publicos, mas normalmente são.
- É a visibilidade padrão no Typescript

- Private (-)
- Utilizada sempre que possível.Torna a visibilidade apenas local(mesmo arquivo), tornando invisivel para outras classes.
- Atributos normalmente são privados
- Metodos que implementam rotinas internas ( metodos auxiliares) devem ser privados.

- Protected (#)
- Torna visivel por classes herdadas( conceito abordado futuramente)
- Utilizado, eventualmente, quando trabalhando com herança.

#### Métodos de acesso
- Tem como unica funcionalidade prover acesso aos atributos privados os quais julgamos que devem ser acessados.
- Cracteristicas:
- REtorno o tipo do atributo que será provido a acesso;
- Não recebe parametro;
- Seu nome é composto pelo prefixo "get" seguido do nome do atributo que o acesso será provido.
- ![image](https://user-images.githubusercontent.com/90521812/138951206-4316f9a1-286e-4fb2-8239-142256d9f3af.png)

#### Metodos modificadores
- Metodod que tem como unica funcionalidade prover modificação aos atributos privados os quais julgamos que podem ser modificados por outras classes.
- Caraceteristicas:
- Não possuem retorno
- Recebe por parametro o valor a ser inserido no atributo;
- SEu nome é composto pelo prefixo "set" seguido do nome do atributo que iremos possibilitar a modificação.
- ![image](https://user-images.githubusercontent.com/90521812/138950391-7efc7672-115e-4bb4-91f8-c3b0bfb82378.png)

#### O motivo
- Porque nos metodos de acesso podemos controlar como a informação será retornada( No caso dos gets) e que tipo de dado será aceito para modificação (No caso sets)

#### Herança
- Exemplo:
- 1 ![image](https://user-images.githubusercontent.com/90521812/139075636-05a06929-11d1-4416-a158-b860748a51e9.png)
- 2 ![image](https://user-images.githubusercontent.com/90521812/139078832-1f8bad6c-2047-4dd9-8086-e8fa305cd0ba.png)
- Posso criar super classes, que serão guarda chuvas com todos os atributos e metodoos em comum para todas essas subclasses, e aí eu deixo na sub classe somente o que é especifico dessa, eliminando assim toda essa redundancia de codigo.
- 3 ![image](https://user-images.githubusercontent.com/90521812/139084880-4a3ada21-385f-4e8e-a9dc-f2ff26e4fe28.png)
- 4 Chamada da super sempre deve ser na primeira linha da super classe
- 5 ![image](https://user-images.githubusercontent.com/90521812/139092998-d4df06f4-6608-4fa0-a1c3-d503c4fa554b.png)
- 6 ![image](https://user-images.githubusercontent.com/90521812/139096545-e4325c55-e87e-4e28-8915-2e0ccf16551d.png)
- Sabemos que precisa de herança quando é um personagem (Precisa de herança) ou tem um atributo ( Composição)
 - Regrinha: "é um"( Herança ) ou "Tem um" ( Composição ).
 - Para não termos extenções da classe é nescessário deixar o constructor privado.
 - ![image](https://user-images.githubusercontent.com/90521812/139101918-182d7040-576c-4dfe-a071-e8ea8b2c21aa.png)

 - 
