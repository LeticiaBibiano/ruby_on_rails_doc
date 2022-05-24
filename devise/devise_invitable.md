# Gem Devise Invitable

[DOCUMENTAÇÃO](https://github.com/scambra/devise_invitable)

+ Essa Gem é uma extensão do Devise, ou seja, devemos obrigatóriamente ter DEVISE em nosso projeto.
+ Sempre que um usuário é cadastrado, um e-mail é enviado para a pessoa.


### Exemplo de CONTROLLER para cadastro de usuário DEVISE:
~~~
class AdministratorManagmentsController < ApplicationController
  layout 'admin'

  before_action :authenticate_administrator!
  before_action :set_resource_name
  before_action :set_resource, only: [:edit, :update, :destroy]

  def index
    @description = 'Lista de todos os administradores do sistema'
    @should_show_new_button = true
    @pagy, @collection = pagy(Administrator.order(created_at: :desc))
  end

  def new
    @description = 'Cadastro de novo administrador'
    @resource = Administrator.new
  end

  def edit
    @description = "Atualização do administrador: #{@resource.email}"

    unless @resource
      flash[:alert] = 'Administrador não encontrado'
      redirect_to administrator_managments_path
    end
  end

  def create
    @resource = ::Administrator.new(resource_params)

    respond_to do |format|
      if @resource.valid?
        if @resource.invite!
          format.html do
            flash[:success] = 'Novo administrador adicionado com sucesso.'
            redirect_to administrator_managments_path
          end
        else
          format.html do
            flash[:alert] = 'Algum erro inesperado ocorreu.'
            render :new, status: :unprocessable_entity
          end
        end
      else
        @description = "Atualização do administrador: #{@resource.email}"
        format.html do
          flash[:alert] = 'Atenção! Verifique os campos inválidos.'
          render :new, status: :unprocessable_entity
        end
      end
    end
  end

  def update
    respond_to do |format|
      if @resource.update(resource_params)
        format.html do
          flash[:success] = 'Administrador atualizado com sucesso.'
          redirect_to administrator_managments_path
        end
      else
        format.html do
          flash[:alert] = 'Atenção! Verifique os campos inválidos.'
          render :new, status: :unprocessable_entity
        end
      end
    end
  end

  def destroy
    @resource.destroy

    respond_to do |format|
      format.html { redirect_to administrator_managments_path, notice: 'Administrador excluído com sucesso.' }
      format.json { head :no_content }
    end
  end

  private

  def set_resource_name
    @title = 'Administradores'
  end

  def resource_params
    params.require(:administrator).permit(:name, :email)
  end

  def set_resource
    @resource = Administrator.find_by(id: params[:id])
  end
end
~~~
