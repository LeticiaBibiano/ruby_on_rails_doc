# Helpers
+ São métodos prontos que podem ser usados nas *views* (front-end). 
+ Esses métodos facilitam a vida do programador, fazendo com que menos código seja escrito para atingir o mesmo resultado.
+ Cada Helper deve ter seu nome ÚNICO e bem específicado, organizar nas pastas corretas.

# Alguns Helpers:

## LINK_TO
*Faz o caminho para o link desejado... utilizar o _path*
~~~
<%= link_to "Nome link que vai aparecer", caminhos_path %>
~~~

## IMAGE (IMG)
*Link para imagem com Ruby, faz a imagem aparecer*
~~~
<%= image_tag coin.url_image, size:"25x25" %> 
~~~

# CRIANDO O PRÓPRIO HELPER! 😙
*Podemos criar nossos próprios helpers de acordo com as nossas necessidades*

⭐ **Dentro da pasta APP/HELPERS**
➡️ Lá dentro você cria os Helpers e depois basta chama-lo em QUALQUER LUGAR do código.

⚠️ ATENÇÃO: ORGANIZAR OS HELPERS EM SEUS DEVIDOS ARQUIVOS, o arquivo **APPLICATION_HELPER** é o "geral" para ser usado em toda a aplicação! 
