Aula Prática de Git – Controle de Versão na Prática
🎯 Objetivo:
Ensinar os alunos a inicializar um repositório, versionar arquivos, usar branches, visualizar histórico, restaurar versões anteriores e fazer push para o GitHub.
🖥️ Pré-requisitos:
- Git instalado na máquina (https://git-scm.com/)
- Conta no GitHub criada
- VS Code ou qualquer editor de texto
- Terminal (cmd, Git Bash ou integrado no VS Code)
📂 1. Criando um novo repositório Git
	$ cd ~/Downloads/Aula_JavaOO
→ Acessar a pasta do seu projeto
	$ git init
→ Inicia o controle de versão no projeto
🔍 Explicação: git init cria um repositório local (oculto na pasta .git), onde o Git começa a controlar as versões dos arquivos.
📌 2. Verificando o status dos arquivos
	$ git status
→ Mostra os arquivos modificados, não versionados ou prontos para serem commitados.
📦 3. Adicionando arquivos para controle de versão
	$ git add JavaOO.zip
→ Adiciona um arquivo específico
	$ git status
→ Verifica novamente o status
	$ git add .
→ Adiciona todos os arquivos modificados
🔍 Explicação: git add nome_arquivo → adiciona um arquivo específico. git add . → adiciona todos os arquivos modificados ou novos para o Git.
✅ 4. Realizando o primeiro commit
	$ git commit -m "commit inicial"
→ Salva uma “foto” atual do seu projeto com uma descrição
👤 5. Configurando nome e email (primeira vez)
	$ git config --global user.email "sua_conta_email@algumacoisa.com"
→ Define o email do autor dos commits
	$ git config --global user.name "Was"
→ Define o nome do autor dos commits
🔍 Explicação: Identifica o autor dos commits localmente (só precisa ser feito uma vez na máquina).
☁️ 6. Conectando ao repositório remoto (GitHub)
	$ git remote add origin https://github.com/seu_repositorio/projeto 
→ Cria um apelido chamado origin que aponta para o repositório no GitHub
🚀 7. Enviando o código para o GitHub
	$ git push --set-upstream origin master
→ Envia a branch atual (master) pela primeira vez e define origem
🔁 8. Alterando e atualizando o projeto
	$ git status
→ Verifica arquivos modificados
	$ git add .
→ Adiciona e prepara os arquivos
	$ git commit -m "Alterações feitas no projeto"
→ Confirma as alterações
	$ git push
→ Envia para o GitHub
📜 9. Verificando histórico de alterações
	$ git reflog
→ Lista todas as ações feitas no repositório
⏪ 10. Voltando para uma versão anterior
	$ git reflog
→ Descubra o código (hash) da versão anterior
	$ git reset --hard <hash_da_versao>
→ Restaura completamente para essa versão
🌿 11. Trabalhando com Branches (ramificações)
	$ git branch
→ Visualizar branches existentes
	$ git branch dev
→ Criar nova branch
	$ git checkout dev
→ Trocar para a nova branch
🔄 12. Merge (Juntando branches)
	$ git checkout master
→ Mudar para a master
	$ git merge dev
→ Juntar branch dev na master
🌐 13. Atualizando projeto com git pull
	$ git pull
→ Baixa e aplica as mudanças do repositório remoto na sua máquina
🛠️ 14. Exemplo prático: Criando e unindo uma branch temporária
	$ git checkout -b sistema-de-login master
→ Criar nova branch a partir da master
	$ git branch
→ Verificar em qual branch estou
	$ git status
→ Verificar mudanças
	$ git add .
→ Adicionar alterações
	$ git commit -m "criado sistema de login"
→ Comitar as alterações
	$ git checkout master
→ Voltar para a master
	$ git pull
→ Atualizar master com servidor
	$ git merge sistema-de-login
→ Unir branch sistema-de-login com a master
	$ git push
→ Enviar para o GitHub
