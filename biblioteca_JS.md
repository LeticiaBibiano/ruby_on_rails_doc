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

+ Baixar a bibioteca
+ Colocar na pasta 📂**app/javascript/packs**
+ Abrimos a pasta no TERMINAL e:
~~~
 💲 wget https://link_da_biblioteca
~~~

