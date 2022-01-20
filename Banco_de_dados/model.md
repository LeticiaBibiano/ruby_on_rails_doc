# Como criar um MODEL:
~~~
💲 rails g model nomeModel descripton:string atributo:tipo #ID quem coloca é o próprio Rails
~~~
*NOME DO MODEL SEMPRE NO SINGULAR!*

+ Cria uma migração e uma tabela (após rodar a MIGRATE, a tabela criada será inserida no banco de dados).

~~~
rails db:migrate
~~~
