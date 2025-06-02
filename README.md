- git clone https://github.com/docker/getting-started-app.git //
**Copia o projeto Docker do GitHub para sua máquina.**

- cd /path/to/getting-started-app //
**Corrigindo diretório do projeto.**

- docker build -t getting-started . //
**Cria uma imagem Docker chamada 'getting-started' usando os arquivos da pasta atual.**

- docker run -d -p 127.0.0.1:3000:3000 getting-started //
**Executei o container em segundo plano (-d) e redirecionei a porta 3000 do container para a porta 3000 do localhost (127.0.0.1). Isso permitiu que a aplicação ficasse acessível via localhost:3000 no navegador.**

- docker ps //
**Executei o docker ps para listar os contêineres.**

{
   - <p className="text-center">No items yet! Add one above!</p>
   + <p className="text-center">You have no todo items yet! Add one above!</p>
}
// **Alterando a mensagem da interface**

- docker build -t getting-started . //
**Criando a versão atualizada do contêiner.**

- docker run -dp 127.0.0.1:3000:3000 getting-started
**Iniciando um novo contêiner com erro, pois a porta 3000 ja está em uso.**

- docker ps
**Listando os contêiners novamente para obter o ID.**

- docker stop <id-do-container>
**Comando para parar o container**

- docker rm <id-do-container>
**Removendo o contâiner.**

- docker run -dp 127.0.0.1:3000:3000 getting-started
**Inciando o contêiner atualizado.**

- **Criei o repositório no Docker Hub.**

- docker push docker/getting-started
**Tentativa falha de enviar a imagem para o docker hub.**

- docker image ls
** Verificação da tag.**

- docker tag getting-started victordevxx/getting-started
**Renomeando a imagem referenciando diretamente no docker hub.**

- docker push victordevxx/getting-started
**Enviando ao docker hub.**
