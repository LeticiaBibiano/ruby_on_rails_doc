# Podemos criar nossas próprias tasks!
~~~
💲 rails g task nome função

💲 rails g task dev setup #exemplo
~~~

*A task será = nome:funcao (dev:setup)

+ Ficará no local **lib/tasks/nome.rake**
+ Exemplo de arquivo:
~~~
namespace :dev do
  desc "TODO"
  task setup: :environment do
                                #ação da task aqui dentro
  end

  desc "Add default administrator" #DESCRIÇÃO DA TASK
  task add_default_admin: :environment do #NOME E AMBIENTE DA TASK
    Admin.create!(
      email: 'admin@admin.com',
      password: '123admin',             #O QUE A TASK FAZ
      password_confirmation: '123admin'
    )
  end

end

~~~

🌟 **%x(comando do terminal)** - *Dessa forma podemos executar comandos do terminal dentro do rails* 

# TTY GEMS
+ É um conjunto de gems focadas em terminal / CLI
+ [Acesse todas as TTY aqui!](https://ttytoolkit.org/)
