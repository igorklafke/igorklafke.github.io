---
layout: post
title: "Baixe legendas automaticamente"
subtitle: "Aplicativo que desenvolvi em Python para fazer download automático a partir do legendas.tv"
category: 
date:       2014-11-17 22:00:00
author:     "Igor Klafke"
header-img: "img/post-bg-default.jpg"

---

Ao contrário de outros sites, o Legendas.tv não disponibiliza uma api para pesquisa fácil de legendas, mas possui um dos melhores acervos em português do Brasil atualmente. Alguns outros sites possuem ferramentas para download automático, mas nem sempre se acha a legenda em português, ou as que tem são mal traduzidas.

Por isso, aproveitando que queria aprender um pouco mais da linguagem de programação Python, desenvolvi um programa para pesquisar automaticamente as legendas baseado nos nomes dos arquivos de vídeo.

O nome, super criativo é LegPy, combiando "legendas" com "python". Um nome horrível merece um [logo horrível](http://www.horriblelogos.com/legpy/), então:

![](/img/horrible-logos-legpy.gif)

###Como funciona

Da seguinte maneira, você executa o aplicativo sobre uma pasta no seu computador e ele pesquisa no Legendas.tv pelo nome de todos os arquivos de vídeo dessa pasta (e pelo primeiro nível de subpastas). Se encontrar a legenda correspondente, o arquivo é baixado automaticamente e copiado para a pasta com o mesmo nome do vídeo.

Arquivos que já possuírem um arquivo de legenda correspondente são ignorados da pesquisa. É impossível eu testar todas as possibilidades de nomes de arquivos, portanto pode haver casos em que a legenda existe mas não seja encontrada, peço que reportem estes casos pelos comentários deste post para que eu possa ajustar o que for necessário.

###Download

A versão para Windows pode ser baixada [AQUI](TODO), após fazer o download, extraia o conteúdo e execute o arquivo install.cmd, serão exibidas mensagens pedindo confirmação apara alterar o registro, clique em sim nas duas. Isso é opcional, mas irá fazer com que uma opção "Procurar Legendas" apareça quando clicar com o botão da direita sobre uma pasta, clicando nesta opção o aplicativo irá procurar legendas para os vídeos desta pasta.

Se você quiser também pode ignorar o passo acima e executar pela linha de comando, passando o caminho para as pastas como parâmetro para o executável. Dessa mesma maneira, é possível criar uma tarefa agendada no Windows para que o aplicativo seja executado automaticamente de tempos em tempos.

Usuários de Mac e Linux podem baixar o código [AQUI](https://github.com/igorklafke/legpy/releases/download/v0.1/legpy.py) e fazer o favor de testar, mas na teoria basta abrir o terminal navegar até a pasta do arquivo legpy.py baixado e executar o seguinte comando:

    python legpy.py <caminho_da_pasta_de_videos>
    
Há uma dependência para o Unrar, que na versão para o Windows coloquei junto no pacote, mas não sei como isso irá se comportar nas outras plataformas.

###Código Fonte

O código fonte está disponível no [Github](https://github.com/igorklafke/legpy), sinta-se a vontade para adimirar o amadorismo do mesmo. E se por acaso quiser contribuir, mandar um *pull request*.