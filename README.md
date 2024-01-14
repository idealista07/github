<!--[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)-->
<h1>Boas Praticas GitHub</h1>	
</br>
#Ferramentas uteis
	<p><a href="https://www.git-scm.com/download/win">git bash</a> -  Interpretador Linux para windows, simula um terminal linux no windows.</p>
	<p><a href="https://vscode.download.prss.microsoft.com/dbazure/download/stable/0ee08df0cf4527e40edc9aa28f4b5bd38bbff2b2/VSCodeUserSetup-x64-1.85.1.exe">vscode</a> -  Compilador de codigo compativel com git, ainda não testei a fundo, em breve trago mais informações</p>
	<p><a href="https://central.github.com/deployments/desktop/desktop/latest/win32">github desktop</a> - Gerenciador para github é possivel fazer todas as operações como commit, pull, branch sem uso de comandos, usando apenas a interface
	grafica, algo que considero muito interessante que é possivel clonar o repositorio modificar e depois aplicar na sua conta do git apartir de uma interface grafica. 
	no meu caso que possuo um servidor de arquivo centralizei tudo em uma pasta e posso modificar mantendo tudo centralizado.</p>

# Configurar login com ssh
	<p>É possivel usar o git cli para alimentar o seu github, para isso é necessario usar conexões por chaves ssh</p>
	<p>Sendo usuarios linux ou windows a pasta .ssh é localizada na pasta de seu usuario</p>
	
	<p>Exemplo Windows: 
			C:\Users\Administrador\.ssh</p>
	<p>Exemplo linux: 
			\home\Administrador\.ssh</p>
	
	<p> Sabendo-se disso criaremos uma chave ssh na pasta .ssh e adicionaremos essa chave na conta</p>

# Gerando chaves ssh
	<p>acessar a pasta .ssh e criar a chave dentro da pasta</p>
	ssh-keygen -t ed25519 -C "your_email@example.com"

	<p>OBS: substituir "your_email@example.com" pelo email usado na conta</p>

# Verifica se a chave ssh está configurada corretamente
	ssh -T git@github.com
	
<h2>Comandos Basicos no git</h2>	
</br>
# Inicia Git
	git init
# Cria arquivo README
	echo "# github" >> README.md  
	<p>Esse arquivo é responsavel pela pagina inicial do repositorio</p>
# Adiciona o arquivo README na fila 
	git add README.md   
# Adiciona um titulo para a nova alteração
	git commit -m "primeiro commit" 
# Informa onde sera feita a alteração
	git branch -M main 
# Aponta o repositorio que sera adicionado a alteração
	git remote add origin git@github.com:idealista07/github.git
# Altera o arquivo na conta
	git push -u origin main