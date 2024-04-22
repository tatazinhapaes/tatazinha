from github import Github

# Autenticação
token = 'seu_token_de_acesso'
g = Github(token)

# Informações do repositório
nome_repositorio = "novo-repositorio"
descricao_repositorio = "Descrição do novo repositório"
repo_privado = False  # Defina como True se quiser um repositório privado


# Criar o repositório
user = g.get_user()
repo = user.create_repo(nome_repositorio, description=descricao_repositorio, private=repo_privado)
print("Repositório criado com sucesso:", repo.html_url)
