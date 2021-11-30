# Instalando Bootstrap na aplicação

~~~
 💲 yarn add bootstrap
~~~
O bootstrap utiliza o Popper para algumas funções, sua instalação é opcional:
~~~
 💲 yarn add popper.js
~~~


+ Ir até 📂**config/webpack/environment.js**
~~~
  const { environment } = require('@rails/webpacker')
  const { default: Popper } = require('popper.js') #Se não instalou Popper essa linha não vai existir

  const webpack = require('webpack')
  environment.plugins.prepend('Provide',
    new webpack.ProvidePlugin({
      $: 'jquery/src/jquery',
      jQuery: 'jquery/src/jquery'
      Popper: ['popper.js', 'default']
    })
  )

  module.exports = environment
~~~

+ Ir até 📂**javascript/packs/application.js** e ADD:
~~~
  import 'bootstrap'
~~~

+ Ir até 📂**assets/stylesheets** e alterar o nome do arquivo *application.css* para **application.scss** (Bootstrap usa SASS!) e ADD:
~~~
  @import "bootstrap/scss/bootstrap";
~~~

# [Documentação Bootstrap em Português](https://getbootstrap.com.br/docs/4.1/getting-started/introduction/)
