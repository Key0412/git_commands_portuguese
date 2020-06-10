# Git para iniciantes  
  
Arquivo criado através do prompt de comando para aprender a fazer submits e commits locais.  
Lembre-se:  
* **git status**: mostra o status dos arquivos no branch  
* **rm**: deleta arquivos  
* **git config user.name**: mostra nome de usuário, pode mostrar email também  
* **git config --list**: mostra todas as configurações locais  
* no VIM, usamos "i" para editar, "esc" para sair da edição, ":w" para escrever, ":q" para sair do editor.  
* **git add <filename>**: adiciona o arquivo ao repositório local (git starts tracking the changes on the archive). Coloca o arquivo em STAGED para então ele sofrer commit (próximo passo). 
* **git commit -m "<descrição das mudanças>"**: faz o commit das mudanças (tira uma snapshot e salva o estado do arquivo). Devolve um número que identifica o estado salvo!  
* **git log --decorate** / **git log** / **git log --author:<nome do autor>** / **git shortlog** / **git shortlog -sn** / **git log --graph**: mostra informações sobre os commits / modificações anteriores  
* **git show <código de um commit anterior, obtido com git log ou semelhante>**: mostra o que houve nesse commit  
* **git diff**: mostra as modificações entre o arquivo modificado atual e o anterior - funciona antes do staging! (antes do git add)   
* **git diff --name-only**: mostra somente o arquivo que foi modificado (antes do git add/stagint)  
* **git commit -am <"Descrição das mudanças>"**: se o arquivo já foi adicionado anteriormente, usa isso pra fazer stage+commit  
* **git checkout <nome do arquivo>**: desfaz as mudanças feitas ANTES DO COMMIT - desfaz mudanças antes da fase de STAGING (antes do git add)  
* **git reset HEAD <nome do arquivo>**: desfaz as mudanças feitas DEPOIS DO STAGING (depois do git add). funciona entre o staging e o commit.  
*  **git reset --soft | --mixed | --hard <código do estado anterior>**: --soft retorna para o estado de staging | --mixed retorna para o estado de modificado | --hard retorna para o estado anterior, remove todas as modificações feitas no arquivo  
* 
