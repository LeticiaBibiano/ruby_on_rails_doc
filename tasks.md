# O que são TASKS?

São tarefas predefinidas que o Rails pode executar.

+ Para listar todas as tasks, execute o comando:
~~~
rails -T
~~~
+ Para filtrar tasks específicas, digite as primeiras letras do que procura, exemplo:
~~~
rails -T db
~~~

# As tasks de BD mais usadas são:

~~~
rails db:create   #cria o db
~~~
~~~
rails db:drop   #apaga o db
~~~
~~~
rails db:migrate   #executa as migrations
~~~
~~~
rails db:rollback   #desfaz a última migration EXECUTADA
~~~
+ Desfazer várias migrations de uma vez:
~~~
rails db:rollback STEP=2
~~~
