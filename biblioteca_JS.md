# Usando uma biblioteca JavaScript na aplicação

# PRIMEIRO INSTALAR JQUERY (Rails 6.0)
~~~
 💲yarn add jquery
~~~

2. Conferir nos arquivos o seguinte:

  ✔️ package.json => "jquery": "^3.3.1",
  
  ✔️ yarn.lock => jquery@^3.3.1:
  
3. No arquivo 📂**config/webpack/environment.js**
~~~
  const webpack = require('webpack')
  environment.plugins.prepend('Provide',
    new webpack.ProvidePlugin({
      $: 'jquery/src/jquery',
      jQuery: 'jquery/src/jquery'
    })
  )
~~~

4. No arquivo 📂**app/javascript/packs/application.js**
~~~
require('jquery')
~~~

# Instalando bibliotecas JS:

## Modo 1: pelo Yarn (RECOMENDÁVEL)

+ [Site YARN (Procure sua biblioteca aqui!](https://yarnpkg.com/)
+ Instala pelo *yarn add nome-biblioteca*
+ Faz require do arquivo em *application.js*
+ **SIGA O EXEMPLO DO JQUERY ACIMA!**


### Modo 2: baixando a biblioteca (não funciona para Rails 6!)

🧧 Dessa forma precisamos COMPILAR os arquivos para dar certo. 

+ Baixar a bibioteca
+ Colocar na pasta 📂**app/javascript/packs**

### Modo 3: pela Gem rails-assets (Antes do Rails 5)

+ [Site da Gem RAILS-ASSETS](https://rails-assets.org/#/)
+ Pesquise no 'search' a biblioteca e instale conforme a documentação do site.
+ Para instalar:
~~~
 💲 bundle install
~~~

