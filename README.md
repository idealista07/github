<!--[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)
Indice
# Boas Praticas GitHub
# Ferramentas uteis
# Configurar login com ssh
# Gerando chaves ssh
# Comandos Basicos no git-->

<h1>Boas Praticas GitHub</h1>	
<h3>Ferramentas uteis</h3>
	<p><a href="https://www.git-scm.com/download/win">Git Bash</a> -  Interpretador Linux para windows, simula um terminal linux no windows.</p>
	<p><a href="https://vscode.download.prss.microsoft.com/dbazure/download/stable/0ee08df0cf4527e40edc9aa28f4b5bd38bbff2b2/VSCodeUserSetup-x64-1.85.1.exe">VSCode</a> -  Compilador de codigo compativel com git, ainda não testei a fundo, em breve trago mais informações</p>
	<p><a href="https://central.github.com/deployments/desktop/desktop/latest/win32">Github Desktop</a> - Gerenciador para github é possivel fazer todas as operações como commit, pull, branch sem uso de comandos, usando apenas a interface gráfica, algo que considero muito interessante é a possibilidade de clonar o repositorio modificar e depois aplicar na sua conta do github posteriormente.</p>

# Configurar login com ssh
É possivel usar o git cli para alimentar o seu github, para isso é necessario usar conexões por chaves ssh, tanto em linux quanto em windows a pasta .ssh é localizada na pasta de seu usuario.
</br>	
- Windows: 
   
		C:\Users\Administrador\.ssh
- Linux:
		
  		\home\Administrador\.ssh
	
Sabendo-se disso criaremos uma chave na pasta .ssh e adicionaremos essa chave na conta

# Gerando chaves ssh
Acessar o repositorio .ssh e usar o comando para criar o par de chaves.

	ssh-keygen -t ed25519 -C "your_email@example.com"
OBS: Substituir "your_email@example.com" pelo email usado na conta

Verifica se a chave ssh está configurada corretamente

 	ssh -T git@github.com
	
<h2>Comandos Basicos no git</h2>	
</br>
Inicia Git
	
 	git init
Cria arquivo README

	echo "# github" >> README.md  
O arquivo README é responsavel pela pagina inicial do repositorio
Adiciona o arquivo README na fila 

 	git add README.md   
Adiciona um titulo para a nova alteração

 	git commit -m "primeiro commit" 
Informa onde sera feita a alteração

 	git branch -M main 
Aponta o repositorio que sera adicionado a alteração

 	git remote add origin git@github.com:idealista07/github.git
Altera o arquivo na conta

 	git push -u origin main
