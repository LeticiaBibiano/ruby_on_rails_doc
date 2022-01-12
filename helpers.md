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

## SELECT
*Para aparecer um seletor(select), onde selecionamos as opções disponíveis*
~~~
select(object, "nome_campo_id", choices = nil, options = {}, html_options = {}, &block)
~~~
+ Exemplo:
~~~
form.select("mining_type_id", MiningType.all.collect { |m| [m.description, m.id] }, { include_blank: "Select..." })
~~~

## FORM_WITH
~~~
<%= form_with(model: [ :nome_do_name_space, @variável_com_dados ]) do |form| %>

<% end %>
~~~


 🔴 **PADRONIZANDO O SELECT AO FLUXO MVC** 🔴
 + Precisamos deixar os dados do MODEL(Banco de Dados) no *controller* e **não diretamente na view**.
 + Devemos criar um método privado (DEF) no controller e dentro do def uma variável de instância (@), para assim, usarmos seu valor na *view*.
 + **Não esquecer do *before_action***
 



# CRIANDO O PRÓPRIO HELPER! 😙
*Podemos criar nossos próprios helpers de acordo com as nossas necessidades*

⭐ **Dentro da pasta APP/HELPERS**
➡️ Lá dentro você cria os Helpers e depois basta chama-lo em QUALQUER LUGAR do código.

⚠️ ATENÇÃO: ORGANIZAR OS HELPERS EM SEUS DEVIDOS ARQUIVOS, o arquivo **APPLICATION_HELPER** é o "geral" para ser usado em toda a aplicação! 
