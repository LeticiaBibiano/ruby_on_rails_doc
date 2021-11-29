+ O Rails carrega todos os controllers através da "tree", ou seja, carrega mesmo a página que não estamos acessando naquele momento.
+ Isso sobregarrega e deixa a aplicação lenta!
+ Devemos compilar cada *assets* com seu *controller* para que sejam carregados separadamente.

# Compilando CSS

1. Remover a linha de código *require_tree* dos arquivos **APPLICATION** na pasta ASSETS (JS e CSS).

2. 🧧Como apagamos a rota tree (que carregava tudo de uma vez), agora vamos fazer carregar APENAS os assets do controller atual (em que a página estará aberta):

+ No arquivo 📂**APP/VIEWS/LAYOUTS/application.html.erb** => Adicionamos as linhas de código

+ Para CSS:
~~~
    <%= stylesheet_link_tag 'application', media: 'all', 'data-turbolinks-track': 'reload' %>
    <%= stylesheet_link_tag params[:controller], media: 'all', 'data-turbolinks-track': 'reload' %>
~~~

🌟 Agora é carregado o CSS E JS application e também a asset do controller atual.

4. Na pasta 📂**config/initializers/assets.rb**:
~~~
    Rails.application.config.assets.precompile += %w( welcome.css coins.css mining_types.css ) #AQUI VAI TODOS OS ARQUIVOS ASSETS/STYLESHEETS
~~~ 
~~~
      Rails.application.config.assets.precompile += %w( welcome.js coins.js mining_types.js ) #AQUI VAI TODOS OS ARQUIVOS ASSETS/JAVASCRIPTS
~~~
*Depois que removemos o require_tree... o Rails só está reconhecendo o assets/application.
