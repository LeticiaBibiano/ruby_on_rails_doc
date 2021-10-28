Antes, temos que entender:

# O que é Active Record?

+ É o **M** do **MVC**, o MODEL.
+ É a camada de software responsável pela lógica de dados e negócio.

[Saiba mais sobre ACTIVE RECORD](https://guides.rubyonrails.org/active_record_basics.html)

# O que é ORM?

+ ORM vem de Object-Relational Mapping.
+ Ou seja, é uma técnica que mapeia os dados em um BANCO DE DADOS para classes/objetos na programação
+ Traduzindo = ORM converte as classes/objetos do nosso projeto em algo que o BANCO DE DADOS entenda.

[Saiba mais sobre Objeto Relacional](https://pt.wikipedia.org/wiki/Mapeamento_objeto-relacional)

**QUEM FAZ O ORM NO RUBY ON RAILS É O ACTIVE RECORD!** (agora fez sentido? 🤓)

# E sobre MIGRATIONS?

+ Em resumo, migrations são características do Active Record (Framework Rails) que serve para "escrever/especificar" as tabelas do BD (Banco de Dados) usando a linguagem Ruby.
+ Chega de usar o SQL, você vai usar as MIGRATIONS!
+ Traduzindo = São as tabelas de dados em Ruby.

⭐ Migrations ficam na pasta *db/migrate/arquivos.rb*

## Importante

➡️ Quando criamos o banco de dados, sua Migration também é criada... ENTÃOOO:

**TEMOS QUE:** "migrar" a Migration para o BD, ou seja, aplicar as mudanças no BANCO DE DADOS (Pois até então, estão apenas no projeto).

🔴 **PARA ISSO:** usamos as **TASKS** predefinidas no Rails.




