# SHA1 🌙

A sigla "SHA" significa *secure hash algorithm* (algoritmo de hash seguro), é um conjunto de funções hash criptográficas projetadas pela NSA (Agência de segurança nacional dos EUA). 
Os dados encriptados geram um conjunto de *characters* identificador de 40 dígitos que são sempre únicos.

## Objetos do Git

Cada objeto consiste em três coisas: um tipo , um tamanho e um conteúdo . O tamanho é simplesmente o tamanho do conteúdo, o conteúdo depende do tipo de objeto e existem quatro tipos diferentes de objetos: "blob", "tree", "commit" e "tag".

- **Blob** — um "blob" é usado para armazenar dados de arquivo - geralmente é um arquivo.

- **Tree** — uma "árvore" é basicamente como um diretório - faz referência a várias outras árvores e/ou blobs (ou seja, arquivos e subdiretórios)

- **Commit** — um "commit" aponta para uma única árvore, marcando-a como a aparência do projeto em um determinado momento. Ele contém meta-informações sobre esse ponto no tempo, como um carimbo de data/hora, o autor das alterações desde o último commit, um ponteiro para o(s) commit(s) anterior(es), etc.

## Comandos GIT básicos

* `git init` —  inicializa um repositório git vazio que, ao ser executado, cria um subdiretório **.git** que contém os arquivos necessários do novo repositório.

* `git add` —  adiciona um arquivo ou pasta à staging area (arquivos que farão parte do seu próximo commit) para ser monitorado.

* `git reset` — desfaz git add todas as alterações antes de um commit.

* `git reset <file>` — desfaz git add de um arquivo específico. 

* `git rm` — remove um arquivo da lista de arquivos monitorados.

* `git status` — exibe o status dos arquivos no repositório (não monitorados, modificados e não salvos, salvos e prontos para commit, etc).

* `git commit` — cria um commit, que é como um snapshot do seu repositório.

* `git branch` — cria ou muda de ramo de desenvolvimento. Também serve para listar todos os ramos existentes.

* `git checkout` — permite navegar entre os branches criados pelo git branch.

* `git merge` — é o jeito do Git de unificar um histórico bifurcado. O comando git merge permite que você pegue as linhas de desenvolvimento independentes criadas pelo git branch e as integre em uma ramificação única.

* `git checkout` — muda de branch (ramo) ou ainda serve para ignorar modificações locais, entre outras funcionalidades.

* `git pull` — busca modificações do repositório remoto.

* `git push` — envia as modificações para o repositório remoto.

* `git clone` — copia um repositório remoto na máquina local.

## configurar uma chave SSH

1. Crie uma nova chave SSH, usando o nome de e-mail fornecido como uma etiqueta.
  * `ssh-keygen -t ed25519 -C "your_email@example.com"`

2. Inicie o ssh-agent em segundo plano.
  * `eval "$(ssh-agent -s)"`

3. Pegue a chave publica acessando a pasta padrão definida
  * `cat ~/.ssh/id_ed25519.pub`

4. Cole a chave na configuração de SSH no github.


___
### ref
[objetos git](http://shafiul.github.io/gitbook/1_the_git_object_model.html) 
