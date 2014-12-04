---
published: false
---

Como expliquei no primeiro post, este blog está hospedado no GitHub Pages, apesar de suportar apenas sites estáticos, é uma alternativa bem útil, pois permite a utilização de um domínio customizado. Neste post vou descrever como criar um site no GitHub.

**Passo 1:** [Criar uma conta](https://github.com/) no GitHub se você ainda não possuir uma, durante a criação da conta escolha o plano _free_.

**Passo 2:** Acesse sua conta no GitHub e [crie um novo repositório](https://github.com/new) com o _Repository name_ seguindo este padrão: _nomeusuario_.github.io. Se a primeira parte do _Repository name_ não for exatamente igual ao seu nome de usuário, a página não irá funcionar. No caso do meu blog por exemplo, como meu nome de usuário no GitHub é igorklafke, o repositório que criei ficou como igorklafke.github.io (posteriormente que eu redirecionei este endereço para o www.igorklafke.com)

Marque a opção _Initialize this repository with a README_ e clique em Create repository.

**Passo 3:** Você agora estará na página inicial do repository, que lista os arquivos do site. Por enquanto só há um README.md, precisamos adicionar o index do site. Para fazer isso clique no "+" ao lado do nome do repositório.

imagem

No campo _Name your file..._ preencha com index.html. E coloque algum conteúdo, por exemplo:

	<!DOCTYPE html>
    <html lang="en">
    <head>
	    <title>Meu site no GitHub</title>
    </head>
    <body>
        Olá, mundo.
    </body>
    </html>

Clique em _Commit new file_.

imagem 2

Você pode adicionar outros arquivos ou editar existentes, clicando sobre o nome do mesmo.

Aguarde alguns minutos (já vi demorar menos de 10 minutos como até uma hora) e acesse endereço com o nome que você deu ao repositório, como http://_nomeusuario_.github.io

**Passo 4:** Se você já possui um domínio customizado (vendido separadamente :)), pode utilizá-lo para o seu site no GitHub. Para isso basta criar na raíz do repositório um arquivo chamado CNAME, utilizando o mesmo procedimento do passo 3. Como conteúdo deste arquivo coloque o seu domínio, no meu caso por exemplo, ficou assim:

imagem do CNAME

Após, no seu servidor de DNS, nas zonas de DNS, adicione uma entrada do tipo CNAME para o seu endereço no GitHub, exemplo:

imagem entrada dns

É isso. Em um próximo post irei explicar como utilizar o Jekyll, que permite criar páginas com templates e que "compilam" para um site estático, caso deste blog.

PS: Se você quiser criar outros sites, não é necessário criar outros usuários no GitHub, você pode simplesmente [criar uma organização](https://github.com/organizations/new) e seguir os mesmos passos utilizando o nome da organização criada no lugar no nome do usuário.