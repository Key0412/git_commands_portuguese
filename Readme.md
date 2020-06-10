# Git para iniciantes  
  
Arquivo criado através do prompt de comando para aprender a fazer submits e commits locais. Veja também este [link](https://wethefoss.github.io/Git-Commands/?Search=git+--version).  
Lembre-se:  
* **mkdir**: cria pasta  
* **rm**: deleta arquivos e pastas   
* **git init**: inicia um repositório na pasta local  
* **git status**: mostra o status dos arquivos no branch   
* **git config user.name**: mostra nome de usuário, pode mostrar email também  
* **git config --list**: mostra todas as configurações locais  
* no VIM, usamos "i" para editar, "esc" para sair da edição, ":w" para escrever, ":q" para sair do editor.  
* **git add *filename***: adiciona o arquivo ao repositório local (git starts tracking the changes on the archive). Coloca o arquivo em STAGED para então ele sofrer commit (próximo passo). 
* **git commit -m *"descrição das mudanças"***: faz o commit das mudanças (tira uma snapshot e salva o estado do arquivo). Devolve um número que identifica o estado salvo!  
* **git log --decorate** / **git log** / **git log --author: *nome do autor*** / **git shortlog** / **git shortlog -sn** / **git log --graph**: mostra informações sobre os commits / modificações anteriores  
* **git show *hash do estado anterior***: mostra o que houve nesse commit  
* **git diff**: mostra as modificações entre o arquivo modificado atual e o anterior - funciona antes do staging! (antes do git add). Pode ser usado com git diff master origin/master para ver diferenças do repo online.  
* **git diff --name-only**: mostra somente o arquivo que foi modificado (antes do git add/stagint)  
* **git commit -am *"Descrição das mudanças"***: se o arquivo já foi adicionado anteriormente, usa isso pra fazer stage+commit  
* **git checkout *nome do arquivo***: desfaz as mudanças feitas ANTES DO COMMIT - desfaz mudanças antes da fase de STAGING (antes do git add)  
* **git reset HEAD *nome do arquivo***: desfaz as mudanças feitas DEPOIS DO STAGING (depois do git add). funciona entre o staging e o commit.  
*  **git reset --soft | --mixed | --hard *hash do estado anterior***: --soft retorna para o estado de staging | --mixed retorna para o estado de modificado | --hard retorna para o estado anterior, remove todas as modificações feitas no arquivo  
* **git push**: depois de configurado, envia as modificações feitas para o GitHub (FAZER AS CONFIGURAÇÕES DE SSH ANTES!). **git push *repo* *branch* ** permite selecionar o branch e o repositório remoto.    
* **git remote** e **git remote -v**: fornecem algumas informações sobre o respositório remoto.  
* **git clone *endereço SSH* *nome do clone***: permite clonar o rep para um rep local.  
* **FORK**: diferente do clone, que permite que uma cópia de um repo de sua propriedade seja copiado, o FORK permite que um repo de outra pessoa seja DIVIDIDO com você, somente assim é possível fazer pedidos (requests) para que as modificações feitas por você sejam aceitas.  
* **git checkout -b *nome do branch***: permite criar um branch  
* **git branch**: permite verificar que branches existem e qual está ativo  
* **git checkout *nome do branch***: muda para o branch  
* **git branch -D *nome do branch***: deleta o branch  
* **git merge *nome do branch***: permite realizar merge entre o branch ativo e o selecionado. merge é uma maneira não destrutiva de unir branches, porém polui um pouco o histórico.  
* **git rebase *nome do branch***: permite enviar a modificação para o topo da lista, porém pode gerar conflitos com outros usuários. Não cria um novo commit como o merge.  
* **merge vs. rebase**: merge cria commits desnecessários, difícieis de ler. rebase é mais limpo. Merge é utilizado em casos de request onde é necessário identificar as linhas unidas. Ao trabalhar e ao adicionar/atualizar novos commits com outros branches, é melhor usar o rebase.  
* **.gitignore**: utilizado para definir que extensões e arquivos devem ser ignorados pelo Git no repositório local.  
* **git stash**: se é um trabalho em desenvolvimento (WIP) e você não deseja o enviar de imediato (stage/commit), é possível guardar estes arquivos modificados em um STASH. Para retornar aos items guardados - **git stash apply**. Para ver que items estão guardados **git stash list**. Para limpar o stash **git stash clear**.  
* **git config --global alias.*atalho* *comando***: permite definir um atalho para o comando em questão.  
* **git tag -a *n_versão* -m *descrição***: permite criar tags com número de versão e descrição. **git push *repo* *branch* --tags**: permite fazer o upload das tags, serão visíveis no campo "Release" do repositório online.  
* **git revert *HashdaVersão***: reverte um commit, no entanto, o faz com um novo commit. Diferente do reset, não deleta o estado anterior, assim é possível continuar a trabalhar nele.  
* **git tag/branch -D ...**: usado para deletar tags e branches locais.  
* **git push origin :*n_versão ou branch***: usado para deletar tags e branches no repo online.  
* **git pull**: obtém arquivos e modificações do repo online, e altera arquivos locais.  
* **git remote show origin**: informa sobre o estado do repo e arquivos, se está out of date também.  
* **git fetch --dry-run**: git fetch somente realiza o download dos novos dados do repo online, mas não integra-os ao seus arquivos.  
