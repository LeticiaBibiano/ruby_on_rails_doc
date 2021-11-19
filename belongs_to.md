# Associações belongs_to
+ Por convenção o Rails exige que o nome do campo seja o MESMO NOME QUE A TABELA, porém no SINGULAR.
+ Campo = Singular
+ Tabela = Plural

# Foreign Key (FK)
+ Quando o arquivo do campo termina em "nome_campo_**id**", significa que isso é uma FOREIGN KEY/chave estrangeira (FK) 
+ OU SEJA, você já sabe que o tal campo está relacionado com uma tabela de mesmo nome, porém no PLURAL.

## Após relacionar as tabelas, precisamos alterar o MODEL:
+ Associamos o Model principal á tabela secundária.
+ **No arquivo do Model Principal (DENTRO DO MODEL:
~~~
    class Coin < ApplicationRecord
      belongs_to :nome_campo
    end
~~~
