# Relacionando/juntando tabelas/CRUD's
+ Podemos unir duas tabelas/CRUD (ou mais)...
+ Para isso fazemos uma **migration STANDALONE** (uma migration a parte)
+ Podemos ADICIONAR UMA MODIFICAÇÃO:
~~~
rails generate migration AddNomeCampoToNomeTabela nome_do_campo:references
~~~
⚠️ O nome sempre deve começar especificado com **AddXXXToYYY**.
+  Podemos REMOVER UMA MODIFICAÇÃO:
~~~
rails generate migration RemoveNomeCampoFromNomeTabela
~~~
⚠️ O nome sempre deve começar especificado com **RemoveXXXFromYYY**.

🧧**ATENÇÃO:** Nome da tabela SEMPRE NO PLURAL!


# Após: Modificamos o MODEL para que fique no novo formato
+ Através do [BELONG_TO]()
