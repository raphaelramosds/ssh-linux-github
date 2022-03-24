# SSH KEY no Linux

Linux users might need to type their username and password everytime they need to run `git push` on bash. In order to avoid this, one should create a SSH connection between their machine and Github. Once this done, that authentication will perform automatically.

For doing so, run the follow script

```bash
bash ./generate.sh "your.github@email.com"
```

Once it's executed, the console will demand you a name for a file it'll put the SSH key. If we only push Enter, its name and location will be `/home/usuário/.ssh/id_rsa`(the standard). Moreover, it'll also require you to type a pass for this key. I personally recomend you to push Enter.

Now, sign in on GitHub, click onto your profile photo locate on right top corner and click Settings. 

Na barra lateral da tela de configuração, clique em SSH and GPG keys.

Ao clicar em SSH key, escolha um título que represente o computador onde a chave está armazenada, copie todo o conteúdo do arquivo id_rsa.pub (armazenado no diretório /home/usuário/.ssh) e cole no campo Key.

Pronto! Agora sempre que você clonar algum repositório do Github, tenha certeza de cloná-lo com o domínio do SSH e não HTTP!

![Tux, the Linux mascot](/ssh-clone.png)
