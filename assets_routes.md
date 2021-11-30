+ Temos várias pastas ASSETS dentro do Rails.

+ O Rails faz uma ÚNICA ROTA VIRTUAL para todas as pastas.

+ A rota virtual feita pelo Rails é sempre substituída pela rota do servidor web (seja lá qual for 🤓), PORTANTO não funciona no modo de PRODUÇÃO.

# Usando TASK para pré-compilar os assets (e resolver a rota acima citada)
~~~
   💲 rails assets:precompile
~~~

+ O Rails levará todos os arquivos assets para dentro de 📂**public/assets**, desse modo os assets vão funcionar no MODO PRODUÇÃO (onde tudo é virtual)

+ Para apagar os assets compilados para MODO PRODUÇÃO:
~~~
   💲 rails assets:clobber
~~~
