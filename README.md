<!--[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)-->
# Inicia Git
  git init
# Cria arquivo README
  echo "# github" >> README.md  
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
# Verifica se a chave ssh está configurada corretamente
  ssh -T git@github.com
