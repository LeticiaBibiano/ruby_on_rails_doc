+ O Rails carrega todos os controllers através da "tree", ou seja, carrega mesmo a página que não estamos acessando naquele momento.
+ Isso sobregarrega e deixa a aplicação lenta!
+ Devemos compilar cada *assets* com seu *controller* para que sejam carregados separadamente.

# Passo a passo

1. Remover a linha de código *require_tree* dos arquivos **APPLICATION** na pasta ASSETS (JS e CSS).
2. Usamos o código:
~~~
    params[:controller] #retorna qual controller está sendo usado
~~~
3. Na pasta 📂**config/initializers/assets.rb**:
~~~
    Rails.application.config.assets.precompile += %w( welcome.css coins.css mining_types.css ) #AQUI VAI TODOS OS ARQUIVOS ASSETS/STYLESHEETS
~~~ 
~~~
      Rails.application.config.assets.precompile += %w( welcome.js coins.js mining_types.js ) #AQUI VAI TODOS OS ARQUIVOS ASSETS/JAVASCRIPTS
~~~
*Depois que removemos o require_tree... o Rails só está reconhecendo o assets/application.
