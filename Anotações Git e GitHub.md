# **Git/GitHub**

**Comandos:** 

	⁃	cd
	⁃	dir
	⁃	mkdir
	⁃	del / rmdir

(Todos esses comandos possuem variantes, chamadas “*flags*” que alteram os comandos, uma dessas *flags* é a “-a” para identificar arquivos ocultos)

(Ao colocar “*” no comando *git add*, ele commita todos os arquivos para o staged)

*Dir* - Comando para dir lista todos os passos, e diretórios onde você está situado

*Cd* - É usado para navegar entre as pastas (use “*cd /*“ para ir para um local específico)
[para voltar é usado “*cd ..*”]

*Mkdir* - Usado para criar uma pasta

*Echo* - “Print” um texto de volta para o terminal (devolve oque você digita)

*Git config* —list - (Você vê as configurações especificas do seu git)

*Del* - Deleta (Delete arquivos)

*Rmdir* - (usado para deletar repositórios)

Comando para limpar a tela: *Cls* ou *Clear*

(Se você apertar Tab o terminal auto completa o código)

(Se você apertar A setinha para cima você re-visita todos os códigos ja usados no terminal)

———————————————————————

**Como Git funciona “Por debaixo dos panos”**

**Sha1**: Algoritmo de interpretação, ele pega o arquivo e embaralha ele de forma específica, a saída dessa encriptação geram um conjunto de caracteres de 40 dígitos, e esse conjunto é único

———————————————————————

**Objetos Internos Git**

O Git é composto por 3 Objetos e dentre eles o:

**Blobs**: É um objeto que contem metadados de códigos e Objetos colocados dentro do Git como; tipo do objeto, tamanho da _string_, tamanho do arquivo e dentre outros (**ele vai ter “\0nomedorarquivo”**) [**não guarda o nome do arquivo, apenas o sha1**]

**Trees**: São usadas para armazenar Blobs, ao contrario dos Blobs as Trees guardam no nome dos arquivos. a Tree é responsável por criar toda as estrutura desse arquivo, mas ela pode apontar para um Blob ou para outra Tree (As Trees também tem um sha1 de vários metadados, se algo mínimo for alterados a alteração reflete tanto no Blob contido na Tree, tanto quanto na própria Tree)

**Commit**: É o Objeto que junta tudo, o Commit aponta para um Parente (ou seja, aponta para o ultimo commit realizado antes dele), aponta para um autor e para a mensagem, ao escrever uma mensagem nesse amontoado de pastas chamado commit você pode dar significado a ele, ele também leva o nome do seu criador, Commit também tem sha1, ao alterar uma blob ele ira gerar um sha1 daquela blob, essa blob por sua vez, tem uma tree apontando para ela,  oque por sua vez vai alterar o sha1 da tree, e o commit que aponta para uma tree também é alterado

**O Git é um dos Sistemas mais seguros e confiáveis!**

———————————————————————

**Chaves SSH**

É uma forma de estabelecer uma conexão segura e encriptada entre duas maquinas

Token de acesso Pessoal: É um token que fica salvo na sua maquina, e sempre que você for criar um Commit o Git irá pedir o seu Usuário e senha e na hora da senha você usa o Token.

———————————————————————

Criando um Commit:

	⁃	Git init (usado para iniciar o repositório do Git)
	⁃	Git Add (usado para mover arquivos e dar comandos)
	⁃	Git Commit (usado para criar um Commit

———————————————————————

**Oque é um arquivo Markdown?**

O arquivo *Markdown*  é uma forma mais humana de se escrever um arquivo HTML

**HTML**: Estrutura Básico de qualquer pagina na WEB

———————————————————————

**Tracked ou Untraked**

Dentro dos arquivos rastreado só pelo Git são os Unmodified (Arquivo que não foi modfificado, Modified(Arquivo que ja foi modificado) e o Staged (Staged são apps que se preparam para fazer parte de outro agrupamento)

(**O Commit coloca todos os códigos de volta para o Unmodified**)

(**Os arquivos Untracked sãos arquivos que o Git ainda não tem conhecimento deles**)

———————————————————————

**Oque um Repositório significa?**

Neste exato momento você tem a separação de dois ambientes, que são:
Servidor e Área Desenvolvimento

	⁃	Servidor: Remote Repository
	⁃	Área de Desenolvilmento: Working Directory, Staging Área, Local Repository

(**Os arquivos sempre vão alterar entre o repositório de trabalho e o staging area**)

Quando você faz um Commit ele começa integrar o seu Repositório Local, e o repositório local por sua vez pode ser empurrado para um Repositório Remoto

(**Porém você só pode fazer esse envio em seu Repositório Local tiver apenas Commits**)

———————————————————————

**Resolvendo Erros no Github**

Ao fazer qualquer alterações mínimas em um Commit e tentar envia-lo ao GitHub ele vai barrar a passagem, para isso é necessário puxa-lo de volta, consertar ele, colocar ele novamente no Stage e após tudo isso envia-lo

Para Clonar um repositório do GitHub:

Basta apenas copiar o link do GitHub, e usar o código *Git Clone LINK QUE VOCÊ COPIOU*
