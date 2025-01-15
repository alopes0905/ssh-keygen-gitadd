# Como criar e definir uma chave SSH
### Criação de chave SSH
1. No terminal, introduzir o comando abaixo.
```bash
ssh-keygen -t ecdsa
```

2. Primir **ENTER** em todas as perguntas seguintes.

3. Foi criada uma pasta .ssh que contem dois ficheiros:
**id_ecdsa** (chave privada) e **id_ecdsa.pub** (chave pública).
É possível verificar a sua criação usando os comandos abaixo.
```bash
cd .ssh
ls -al
```

### Definir a chave SSH no GitHub
1. Fazer Login na conta GitHub no Browser.

2. No canto superior direito, clicar no **Ícone do perfil** e, de seguida, selecionar **Definições**.

3. Nas opções do lado esquerdo, escolher **SSH and GPG keys**.

4. Debaixo do menu SSH Keys, escolher **New SSH Key**.

5. Colocar o conteúdo do ficheiro *id_ecdsa.pub* em **Key** e definir um **Title** (apenas servirá para ajudar distinguir as chaves SSH, no caso de haver mais do que uma).

6. Após selecionar **Add SSH Key** deverá aparecer criada a chave associada ao título escolhido.

7. Pode ser necessário definir o git local do computador. Para isso, basta executar os comandos abaixo no terminal.
```bash
git config --global user.name "Name Example"
git config --global user.email example@email.com
```
## Parabéns, está tudo pronto.
