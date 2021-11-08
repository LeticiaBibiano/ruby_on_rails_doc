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
