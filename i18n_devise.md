## Para o que criamos com Devise, devemos usar o i18n da seguinte forma:

+ O Devise, por padrão, sempre estará em INGLÊS.

+ Para **PORTUGUÊS-BR**, fazemos:

1. Em 📂'config/locales/', criar arquivo com o nome de 'devise.pt-BR.yml'.
2. Em 📂'config/application.rb', utilize => config.i18n.default_locale = :'pt-BR'
3. Cole o seguinte código com as configurações:

~~~lang-yml
pt-BR:
  devise:
    confirmations:
      confirmed: "Sua conta foi confirmada com sucesso."
      send_instructions: "Você receberá um e-mail para confirmar sua conta em alguns minutos."
      send_paranoid_instructions: "Caso seu endereço de e-mail já exista em nosso banco de dados, você receberá um email com instruções sobre como ativar sua conta."
    failure:
      already_authenticated: "Você já está logado."
      inactive: "Sua conta ainda não foi ativada."
      invalid: "Email ou senha inválidos."
      locked: "Sua conta está bloqueada."
      last_attempt: "Você possui apenas uma tentativa, antes de sua conta ser bloqueada."
      not_found_in_database: "Email ou senha inválidos."
      timeout: "Sua sessão expirou, faça login novamente para continuar."
      unauthenticated: "Você precisa fazer login ou se registrar, antes de continuar."
      unconfirmed: "Você precisa confirmar sua conta, antes de continuar."
    mailer:
      confirmation_instructions:
        subject: "Instruções de confirmação"
      reset_password_instructions:
        subject: "Instruções para redefinir sua senha"
      unlock_instructions:
        subject: "Instruções para desbloquear sua conta"
      password_change:
        subject: "Senha modificada"
    omniauth_callbacks:
      failure: "Não foi possível autenticá-lo em %{kind} por causa de \"%{reason}\"."
      success: "Autenticado com sucesso em %{kind}."
    passwords:
      no_token: "Você não pode acessar essa página para redefinir sua senha. Se você recebeu um e-mail para redefinir sua senha, por favor, certifique-se de estar usando a URL correta."
      send_instructions: "Você receberá um e-mail com instruções sobre como redefinir sua senha em poucos minutos."
      send_paranoid_instructions: "Se o seu endereço de e-mail existir em nosso banco de dados, você receberá um link de recuperação de senha em poucos minutos."
      updated: "Sua senha foi alterada com sucesso. Você agora está conectado."
      updated_not_active: "Sua senha foi alterada com sucesso."
    registrations:
      destroyed: "Até logo! Sua conta foi cancelada com sucesso. Nós esperamos vê-lo novamente em breve."
      signed_up: "Bem-vindo! Você se registrou com sucesso."
      signed_up_but_inactive: "Você se registrou com sucesso. Para efetuar login, você deverá ativar sua conta."
      signed_up_but_locked: "Você se registrou com sucesso. No entanto, não podemos logá-lo, pois sua conta está bloqueada."
      signed_up_but_unconfirmed: "Uma mensagem com um link de confirmação foi enviado para seu endereço de e-mail. Por favor, verifique-o, para ativar sua conta."
      update_needs_confirmation: "Você atualizou sua conta com sucesso, mas precisamos verificar o seu novo endereço de e-mail. Por favor, verifique seu e-mail e clique no link de confirmação para confirmar o seu novo endereço de e-mail."
      updated: "Sua conta foi atualizada com sucesso."
    sessions:
      signed_in: "Logado com sucesso."
      signed_out: "Saiu com sucesso."
      already_signed_out: "Saiu com sucesso."
    unlocks:
      send_instructions: "Você receberá um e-mail com instruções sobre como desbloquear sua conta, em poucos minutos."
      send_paranoid_instructions: "Se a sua conta existir, você receberá um e-mail com instruções sobre como desbloqueá-la, em poucos minutos."
      unlocked: "Sua conta foi desbloqueada com sucesso. Faça login para continuar."
  errors:
    messages:
      already_confirmed: "já foi confirmado, por favor, efetue login"
      confirmation_period_expired: "deve ser confirmada dentro de %{period}, por favor solicite uma nova"
      expired: "expirado, por favor solicite uma nova"
      not_found: "não encontrado"
      not_locked: "não encontra-se bloqueada"
      not_saved:
        one: "1 erro impediu a gravação de %{resource} :"
        other: "%{count} erros impediram a gravação de %{resource} :"
~~~


