# **COMANDOS GIT:**

·     **DIR ->** LISTAR. Se situar dentro de um sistema operacional e entender qual local estamos. Traz uma lista de diretórios contidos na pasta no qual estamos situados. Ou seja, dentro de C>users>fe_fa> tem todas as pastas listadas.

·     **CD ->** como desço o nível nesses diretórios? Como vou para uma pasta específica dentro do sistema operacional? Pelo CHANGE DIRECTORY (CD). Comando que possibilita que naveguemos por entre as pastas. CD/ -> leva para a pasta Diretório (C). CD WINDOWS -> para a pasta Windows. Para retroceder, usamos C..

·     **CLS ->** Clear Screen. Comando para limpar a tela do diretório.

**ATALHO ÚTIL DO TECLADO -> TAB -> função de autocompletar.** Ex: Se escrever CD W e apertar TAB, ele já reconhece que na pasta que eu estou tem uma pasta chamada Windows, e autocompleta o nome para mim.

·     **MKDIR -**> Make Directory. Criar pasta de diretório.

·     **ECHO -**> “Printa” de volta no terminal uma frase ou texto. Devo usar o **>** (redirecionador de fluxo), ou seja, pega a saída do meu echo **e joga em um arquivo. Para criar arquivo**: echo hello > hello.txt.

·     **ECHO > “nome do arquivo (Ex: README.MD) -**> cria um arquivo

·     **DEL -**> deleta ARQUIVOS. Uso para deletar o que tem dentro de uma pasta, mas não deleto a pasta.

·     **RMDIR** -> deleta o depositório/a pasta. OBS: escrever rmdir “nome pasta” /S /Q.

OBS: No sistema Linux -> -RM -RF -> R de recursivo (dentro da pasta, pode existir várias outras, o que significa que apagarei todas elas) e o F é de FORCE (para não aparecer nenhum tipo de confirmação para deletar ou não a pasta).

·     **OPENSSL SHA1 “nome do arquivo” ->** visualizar a sha1 do arquivo

·     **ECHO “NOME ARQUIVO” | GIT HASH-OBJECT --STDIN ->** mostra o código sha1 do arquivo

·     **ECHO -E “nome do blob\o que eu quero saber (conteúdo/tamanho/texto) | openssl sha1 ->** saber o sha1 de um dos atributos do blob.

·     - **git init** -> iniciar o repositório GIT;

·     - **git add** **“nome do arquivo”** -> mover arquivo e dar inicio ao versionamento e conhecer os primeiros comandos;

·        - **git add \* ou git add . ->** adicionar tudo o que está no working directory e adiciona para staged, para podermos commitar.

·     - **git commit** **-m “frase que explica a alteração para novo commit”** (Ex: adiciona index) -> criar o primeiro commit;

·        - **git commit -m “commit inicial”** -> criar um commit inicial

·     - **ls -a** -> mostra arquivos ocultos;

·     **- cd /\*nome da pasta que eu quero\*** -> muda a pasta

·     **- cd ..** -> volta pra pasta superior

·     - **git config --global user.email “****[fernandaathanazio@gmail.com](mailto:fernandaathanazio@gmail.com)****”** e **git config --global user.name Fernanda** -> configurar git antes de começar a usar

·     **GIT STATUS** **->** demonstra os status do arquivo (unmodified, modified e staged). Comando usado com muita frequência.

·     **MV “nome do arquivo/pasta” ./”nome do outro repositório” (Ex: mv strogonoff.md ./receitas/) ->** mover arquivo ou pasta para outro local.

**Obs: toda vez que modificar o arquivo ou coloca-lo em outro local, usar: git add para manda-lo para staged.**

·     **GIT RM “nome do arquivo” ->** mover arquivos para unmodified.

·     **GIT RESTORE --STAGED “NOME DO ARQUIVO” ->** retirar os arquivos do modo staged.

·     **GIT CONFIG --LIST ->** lista todas as configurações específicas do meu git.

·     **GIT CONFIG --GLOBAL --UNSET USER.NAME/USER.EMAIL ->** para deletar o nome de usuário e email. Após, devo configurar novo usuário e/ou email.

·     **GIT REMOTE ADD ORIGIN “ENDEREÇO HTTPS GERADO GITHUB” ->** cadastra um repositório remoto.

·     **GIT REMOTE -V** -> lista as listas de repositórios remotos cadastrados.

·     **GIT PUSH ORIGIN MAIN** -> envia o diretório local para o remoto.

·     **GIT PULL ORIGIN MAIN** -> puxa as duas ou mais versões do arquivo para um único. Se der algum conflito de merge, entrar no arquivo, modificar e salvar a versão final. Após, git add * e git commit -m “resolve conflitos”. Após empurra pro GitHub (git push origin master).

·     **GIT CLONE \*endereço https retirdo do GitHub ->\*** usar para copiar um github de outra pessoa para minha máquina

 

**Comando para gerar Chave de Acesso e coloca-la no GitHub – escrever nessa ordem:**

·     **ssh-keygen -t ed25519 -C** **[fernandaathanazio@gmail.com](mailto:fernandaathanazio@gmail.com)** -> gerar chave sha1

**cat id_ed25519.pub** **->** comando para visualizar conteúdo de uma das chaves. A chave que aparecer é a que será colocada no GitHub.

·     **eval “$(ssh-agent -S)” ->** pegar as chaves e lidar com elas. Irá gerar um **agente pid.**

·     **ssh-add id_ed25519 ->** a chave que gerar, colo no GitHub.

  

#### Ordem para usar:

1-   git clone *endereço github*

2-   cd *nome da pasta/repositorio*

3-   git status (pra ver se tá tudo bem)

4-   quando criar novos arquivos/pastas e mandar para o GitHub -> git add *

5-   git commit -m “*colocar comentário sobre o commit, que tenha sentido sobre o que eu quero enviar”*

6-   git push origin main