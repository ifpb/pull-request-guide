# Guia do Pull Request

Este repositório foi criado no intuito de introduzir o conceito de Pull Request (PR) para projetos da organização do IFPB do Github. Segundo o Github, [a ideia do PR](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) consiste em uma ação que facilitla a colaboração entre desenvolvedores em projetos da plataforma por meio da sugestões de mudança de código, usando um processo de diálogo e revisão com os administradores do repositório.

O Github define um passo a passo de como [criar um PR](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request), e para facilitar a compreensão destas etapas será exibido a seguir alguns passos necessários para sugerir mudanças no repositório [ifpb/pull-request-guide](https://github.com/ifpb/pull-request-guide), sendo mais específico, será criado um PR para incluir um novo arquivo chamado `users/luiz.chaves.txt`:

**PASSO 1** - Acesse o repositório desejado para criar um PR, que neste caso será este próprio (https://github.com/ifpb/pull-request-guide):

![Repositório ifpb/pull-request-guide](assets/ifpb-pull-request-guide.png)

**PASSO 2** - Para contribuir é necessário criar uma cópia por meio de um fork, então primeiro passo será fazer o login na sua conta do Github e depois acione o botão `fork`:

![Fork](assets/fork.png)

O resultado desta ação será a criação do repositório https://github.com/lucachaves/pull-request-guide, contudo, verifique que no seu caso o fork vai gerar uma URL diferente:

![Repositório lucachaves/pull-request-guide](assets/lucachaves-pull-request-guide.png)

**PASSO 3** - Concluido a etapa do fork a sua cópia já foi criada, nela você possui permissão para fazer alterações, entretanto, essas alteração podem ser feitas a partir do seu computador, então para baixar sua cópia clone o repositório para o seu computador:

```
$ git clone https://github.com/lucachaves/pull-request-guide.git
```

Observe que a URL do seu fork é diferente, então faça alteração no comando git clone.

**PASSO 4** - Ao clonar um repositório, deve-se configurar o seu nome e email no clone:

```
$ git config user.name "Luiz Carlos"
$ git config user.email lucachaves@gmail.com
```

**PASSO 5** - Depois que o clone foi configurado é possível iniciar as sugestões de alteração;

```
$ echo "Luiz Carlos Rodrigues Chaves" > luiz.chaves.txt
```

**PASSO 6** - Registre no git as mudanças realizadas (delta):

```
$ git add luiz.chaves.txt
$ git commit -m 'descrição da muda'
```

Caso seja necessário incluir mais de um arquivo no registro de mudança de forma automática, é possível usar o comando:

```
$ git add -A
```

ou 

```
$ git add .
```

**PASSO 7** - Registrado a mudança no clone, vamos enviá-lo para o seu fork (Neste exemplo será enviado para https://github.com/lucachaves/pull-request-guide):

```
$ git push -u origin master
```

As próximas submissões pode ser enviada com o comando:

```
$ git push
```

**PASSO 8** - Pronto, o Github já recebeu sua mudança no fork (https://github.com/lucachaves/pull-request-guide), falta enviar a mudança como uma contribuição para o repositório original (https://github.com/ifpb/pull-request-guide) usando o Pull Request:




**PASSO 9** - Se no PR for solicitado alguma mudança ou se foi dectado a necessidade de mudanças de arquivo, faça a mudança necessária e em seguida repita os Passos 6 e 7. Quanto ao PR, só é preciso criar um novo caso o PR anterior tenha sido fechado.
