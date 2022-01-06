# Criando LOGIN e SENHA para o Administrador e Usuário padrão

## ADMINISTRADOR:
*Esse é um código da GEM DEVISE*
~~~
 Admin.create!(
      email: 'admin@admin.com',
      password: '123admin',
      password_confirmation: '123admin'
    )
~~~

## USUÁRIO
~~~
  User.create!(
        email: 'user@user.com',
        password: '123user',
        password_confirmation: '123user'
      )
~~~
