---
layout: post
title: "Baixando legendas automaticamente"
subtitle: "Aplicativo que desenvolvi em Python para fazer download automático a partir do legendas.tv"
category: 
date:       2014-12-08 22:50:00
author:     "Igor Klafke"
header-img: "img/post-bg-default.jpg"

---

Ao contrário de outros sites, o Legendas.tv não disponibiliza uma API para pesquisa fácil de legendas, mas possui um dos melhores acervos em português do Brasil atualmente. Alguns outros sites possuem ferramentas para download automático, mas nem sempre se acha a legenda em português, ou as que existem estão mal traduzidas.

Por isso, aproveitando que queria aprender um pouco mais da linguagem de programação Python, desenvolvi um aplicativo para pesquisar automaticamente as legendas pelos nomes dos arquivos de vídeo.

O nome, super criativo é LegPy, combinando "legendas" com "python". Um nome horrível merece um [logo horrível](http://www.horriblelogos.com/legpy/), então:

![](/img/horrible-logos-legpy.gif)

###Como funciona

Da seguinte maneira, ao executar o aplicativo pela primeira vez será solicitado seu usuário e senha do Legendas.TV, após fazer o login, você digita o caminho da pasta onde estão os seus vídeos e clica em buscar (as próximas vezes que o aplicativo for executado este campo já virá preenchido com o último valor). O aplicativo irá pesquisar no Legendas.tv pelo nome de todos os arquivos de vídeo dessa pasta (e pelo primeiro nível de subpastas). Se encontrar a legenda correspondente, o arquivo é baixado automaticamente e copiado para a pasta com o mesmo nome do vídeo.

Arquivos que já possuírem um arquivo de legenda correspondente serão ignorados da pesquisa. É impossível eu testar todas as possibilidades de nomes de arquivos, portanto pode haver casos em que a legenda existe mas não seja encontrada, peço que reportem estes casos pelos comentários deste post para que eu possa ajustar o que for necessário.

**Aviso:** O usuário e senha ficarão salvos em um arquivo chamado settings.conf na mesma pasta do executável.

###Download


A versão para Windows pode ser baixada [AQUI](https://github.com/igorklafke/legpy/releases/download/v0.2/legpy-v0.2.zip), após fazer o download, extraia o conteúdo e execute o arquivo legpy.exe.

Usuários de Mac podem seguir o procedimento para Linux abaixo ou aguardar eu gerar um *release* para esta plataforma um dia.

Usuários de Linux podem baixar o código [AQUI](https://github.com/igorklafke/legpy/archive/v0.2.tar.gz) e tentar usar, navegando até a pasta do arquivo legpy.py e executando a seguinte linha de comando:

    python legpy.py

Existem dependências que precisam ser resolvidas, mas já que você usa linux deve conseguir se virar, né?
    
Também há uma dependência para o Unrar, que na versão para o Windows coloquei junto no pacote, mas não sei como isso irá se comportar nas outras plataformas.

###Código Fonte

O código fonte está disponível no [Github](https://github.com/igorklafke/legpy), sinta-se a vontade para adimirar o amadorismo do mesmo. E se por acaso quiser contribuir, mandar um *pull request*.