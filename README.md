# SSH KEY no Linux

Quando usamos uma distribuição Linux pela primeira vez e tentamos rodar `git push` nos nossos repositórios, precisamos sempre informar o username e a senha do Github. Para evitar essse processo repetitivo, criamos uma conexão SSH entre nossa máquina e o Github para que tal autenticação seja feita automaticamente.

Para tal, rode o seguinte script 

```bash
bash ./generate.sh <Email do Github>
```

Depois de executado, o programa solicitará um nome de arquivo para a chave SSH. Se apenas pressionarmos Enter, o nome e a localização padrão serão utilizados (/home/usuário/.ssh/id_rsa). Após isso, também será solicitada uma senha para a chave, recomendo que apenas clique Enter - deixando vazio.

Agora, faça login no GitHub, clique na foto de perfil no canto superior direito e escolha a opção Settings. Na barra lateral da tela de configuração, clique em SSH and GPG keys.

Ao clicar em SSH key, escolha um título que represente o computador onde a chave está armazenada, copie todo o conteúdo do arquivo id_rsa.pub (armazenado no diretório /home/usuário/.ssh) e cole no campo Key.

Pronto! Agora sempre que você clonar algum repositório do Github, tenha certeza de cloná-lo com o domínio do SSH e não HTTP!

![Tux, the Linux mascot](/ssh-clone.png)