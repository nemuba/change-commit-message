# Como alterar a mensagem do commit ?

Se por engano você escreveu a mensagem do **`git commit -m "mensagem errada"`** errado, existe um comando chamado **`git rebase -i HEAD~n`**. ( AINDA BEM !!! )

### *1º PASSO*: SABER ONDE ESTÁ LOCALIZADO SEU COMMIT.
--------------------------------------------------

Mas antes de alterar a mensagem do **`commit`**, você precisa saber qual é a posição do commit na ordem cronológica. Pra isso basta rodar o comando **`git log --oneline`**, aparecerá algo assim:

**`93ed9ab message 1` -> ultimo commit.**

`93ed9ab message 2`

`93ed9ab message 3`

**`93ed9ab message 4` -> mensagem errada !**

Agora sabemos a posição da mensagem !

### *2º PASSO*: RODE O COMANDO DE ALTERAÇÃO
-------------------------------------------
Para atualizarmos a messagem desse commit na posição 4, precisamos rodar o comando na seguinte forma: **`git rebase -i HEAD~4`**.

A seguir abrirá um arquivo no seu terminal uma sequência de commits da seguinte forma:

**`pick 93ed9ab message 4` -> commit com a mensagem errada!**

`pick 93ed9ab message 3`

`pick 93ed9ab message 2`

`pick 93ed9ab message 1`

### *3º PASSO*: SETAR O COMMIT QUE DESEJA ALTERAR A MENSAGEM.
------------------------------------------------

Para mudarmos a mensagem  do commit precisamos mudar a palavra **`pick`** por **`reword`** na mensagem que iremos alterar, ficando da seguinte maneira:

### ! Dica para inserir ou editar arquivo no git bash do windows:
1- No terminal:
* Aperte a tecla **`I`** e comece a editar o arquivo.
* Ao terminar de editar ou inserir, aperte a tecla **`ESC`**, e em seguida para salvar a edição digite **`:wq`** e tecle **`ENTER`**.

Após a alteração ficará assim:

**`reword 93ed9ab message 4` -> commit com a mensagem errada!**

`pick 93ed9ab message 3`

`pick 93ed9ab message 2`

`pick 93ed9ab message 1`

Em seguida salve o arquivo e feche o mesmo.

### *4º PASSO*: ALTERE A MENSAGEM DO COMMIT

Logo em seguida abrirá novamente outro arquivo para edição da mensagem do commit, aparecendo da seguinte maneira:

**`message 4`**

 Siga os passos anteriores para editar e salvar o arquivo e pronto mensagem do commit alterada. \o/

 ### *5º E ULTIMO PASSO*:MANDE AS ALTERAÇÕES PARA O GITHUB FORÇANDO O **`git push`**.
 -------------------------------------------------

 Agora precisamos mandar o commit com a mensagem alterada para o github. Rode o seguinte comando:

 **`git push --force`**

 Pronto alteração da mensagem concluida e disponivel no servidor remoto ! . \o/


 #### **PARABENS !!!**
 #### **BONS ESTUDOS !**
 -------------------------------------------------

 **Autor:** Alef Ojeda de Oliveira.

 **github:** [nemuba](https://github.com/nemuba).

 **linkedin:** [alef-ojeda](https://www.linkedin.com/in/alef-ojeda/).