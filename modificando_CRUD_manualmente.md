# Podemos modificar algum dado que esteja errado no CRUD...
+ Usando o: 
~~~
rails db:rollback
~~~
e apagando o CRUD criado para refazer da maneira correta...
🧧 **APENAS QUANDO O ERRO FOR PERCEBIDO NA HORA E NÃO AFETARÁ NENHUM DADO**

# Podemos modificar MANUALMENTE alterando os arquivos

1- Arquivo *MIGRATION* = 📂 **db/migrate/arquivo.rb**
2- Todos os arquivos **VIEW** do CRUD.
3- O arquivo **CONTROLLER** do CRUD.
