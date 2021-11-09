# Acessar o Console:
~~~
rails console
~~~
~~~
rails c
~~~
# Mexer nos dados sem alterá-los:
~~~
rails console --sandbox
~~~
## Testes com .APP
*Testa as rotas da aplicação*
~~~
app.root_path
~~~
## Testes com .HELPER
*Testa os helpers padrão e criados*
~~~
helper.link_to "teste", "/teste"
helper.data_br(Date.today)
~~~
# MODELS
+ No Rails Console podemos trabalhar com qualquer model, usando seu nome e os métodos Active Record disponíveis.
+ Exemplo
~~~
Nome.first # Retorna o primeiro elemento
~~~
~~~
Nome.last # Retorna o último elemento
~~~
~~~
Nome.all # Retorna todos os elementos em um ARRAY
~~~
# Criando um novo elemento:
+ Nome da variável = NomeModel.new
+ var.description = "Bitcoin"
+ var.url_image = "http://"
+ var.save! **COM ! NO FINAL PARA MOSTRAR POSSÍVEIS ERROS!"
~~~
var = NomeModel.create! (
  description: "Bitcoin",
  url_image: "https://"
)
~~~
