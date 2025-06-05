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

- docker run -dp 127.0.0.1:3000:3000 getting-started //
**Iniciando um novo contêiner com erro, pois a porta 3000 ja está em uso.**

- docker ps //
**Listando os contêiners novamente para obter o ID.**

- docker stop <id-do-container> //
**Comando para parar o container**

- docker rm <id-do-container> //
**Removendo o contâiner.**

- docker run -dp 127.0.0.1:3000:3000 getting-started //
**Iniciando o contêiner atualizado.**

- **Criei o repositório no Docker Hub.**

- docker push docker/getting-started //
**Tentativa falha de enviar a imagem para o docker hub.**

- docker image ls //
**Verificação da tag.**

- docker tag getting-started victordevxx/getting-started //
**Renomeando a imagem referenciando diretamente no docker hub.**

- docker push victordevxx/getting-started //
**Enviando ao docker hub.**

- docker run --rm alpine stat greeting.txt //
**Verifiquei as propriedades do arquivo greeting.txt num container Alpine temporário que desaparece após a execução.**

- docker run --rm alpine stat greeting.txt //
**Executei um novo contêiner alpine e logo a´pós usei o stat para verificar se existia.**

- docker volume create todo-db //
**Criando um volume usando o comando acima.**

- docker run -dp 127.0.0.1:3000:3000 --mount type=volume,src=todo-db,target=/etc/todos getting-started //
**Subi o container em background com acesso pela porta 3000 e criei um volume persistente para armazenar dados.**

- docker ps //
**Novamente para pegar o id do serviço.**

- docker rm -f id //
**Para então removê-lo.**

- docker volume inspect todo-db //
**Indo a fundo para entender armazenamento de dados do Docker.**

- docker run -it --mount type=bind,src="$(pwd)",target=/src ubuntu bash
**Subi um Ubuntu temporário com acesso à sua pasta atual, pra você poder trabalhar direto no terminal dele.**

- **Entrei na pasta src e criei um arquivo myfile.txt**

-docker run -dp 127.0.0.1:3000:3000 \
    -w /app --mount type=bind,src="$(pwd)",target=/app \
    node:18-alpine \
    sh -c "yarn install && yarn run dev"
**Criei um container Node.js com sua pasta do projeto sincronizada, instalei as dependências e levantei o servidor de desenvolvimento de forma automatizada.** 

- docker network create todo-app
**Criei uma rede Docker nova chamada todo-app para isolar a comunicação entre containers.**

- ** defini as variáveis de ambiente que o banco de dados utilizará.**

- docker ps
**para verificar o id do conteiner mysql.**

- docker exec -it <mysql-container-id> mysql -u root -p
**verificando se o banco de dados está instalado e em normal funcionamento.**

- docker run -it --network todo-app nicolaka/netshoot
**Inicie um novo contêiner usando a imagem nicolaka/netshoot.**

- dig mysql
**procurando o endereço ip**

- docker exec -it <mysql-container-id> mysql -p todos
**Verificando banco de dados.**

- mysql> select * from todo_items;
**selecionando os itens do banco de dados.**

- **Criação do arquivo compose no VS CODE.**

- docker compose up -d
**Iniciando a pilha de aplicativos.**

- docker image history getting-started
**Visualizando as imagens que criei.**

- docker image history --no-trunc getting-started
**Adição de comando para ver a lista completa.**

- docker build -t getting-started .
**Criando uma nova imagem.**

**Finalização do workshop analisando "O que vem a seguir".**
