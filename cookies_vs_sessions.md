# Cookies X Sessions

+ **Cookies:** Armazena dados no navegador(servidor WEB).
+ **Sessions:** Armazena dados no servidor.

## Criando:

**NO CONTROLLER**

+ Cookies:
~~~
    cookies[:nome] = "dados a armazenar"
~~~

+ Sessions:
~~~
    sessions[:nome] = "dados a armazenar"
~~~

## Usando:

+ Cookies:
~~~
    <%= cookies[:nome] %>
~~~

+ Sessions:
~~~
    <%= session[:nome] %>
~~~
