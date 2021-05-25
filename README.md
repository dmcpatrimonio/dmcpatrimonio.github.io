# Documentação, Modelagem e Conservação do Patrimônio #

![](https://github.com/dmcpatrimonio/arqtrad/workflows/Website/badge.svg?branch=master)

Site do grupo de pesquisa. Usamos:

- [Jekyll](https://jekyllrb.com)
- Template [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
- [Academicons](http://jpswalsh.github.io/academicons/)

## Como atualizar este site ##

Antes de mais nada, crie uma conta no [GitHub](https://github.com) e
informe aos líderes do grupo o seu nome de login. Os líderes vão lhe
enviar um convite para se tornar membro da equipe e poder editar este
site — preste atenção às suas notificações nesta plataforma!

> :wink: Dica: cadastre-se com o e-mail institucional da sua
> universidade para desbloquear recursos adicionais como repositórios
> privados :bangbang: Se você já se cadastrou com outro e-mail, pode
> adicionar o endereço institucional clicando no seu ícone no alto à
> direita desta tela, depois `Settings > Email`.

Depois de aceitar o convite dos líderes, você poderá começar a propor
edições neste e noutros repositórios do grupo de pesquisa.
Após atualizar qualquer página, o site leva alguns minutos para ser
atualizado. Instruções específicas:

* * * *

1. [Notícias e outras postagens](#notícias-e-outras-postagens)
2. [Novo membro](#novo-membro)
3. [Novo projeto de pesquisa](#novo-projeto-de-pesquisa)
4. [Nova produção bibliográfica ou técnica](#nova-produção-bibliográfica-ou-técnica)

Para editar dados existentes, siga as mesmas instruções mas localize as
páginas e os registros existentes em vez de criar novos.

* * * *

## Notícias e outras postagens ##

Crie uma página no endereço
[`_posts/2021-02-28-titulo-resumido.md`](_posts/) seguindo (copiando) o
modelo abaixo e alterando o conteúdo.

O nome do arquivo deve começar com a data no formato `aaaa-mm-dd` e na
sequência um breve nome explicativo (não precisa ser idêntico ao
título), tudo em caixa baixa e sem acentos ou espaços (use hífens para
separar os elementos e as palavras do nome). O nome do autor indicado no
topo do arquivo, este sim, precisa ser idêntico ao nome do pesquisador
tal como cadastrado no arquivo [`_data/authors.yaml`](_data/authors.yaml)
(saiba mais abaixo, na seção [Novo membro](#novo-membro)).

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` yaml
---
title: Título completo do post numa linha só
# O nome do autor abaixo deve ser idêntico ao cadastrado
# conforme instruções da seção 'Novo membro'
author: Nome do autor
date: 2021-02-28
---
```
``` markdown
# Isto é um cabeçalho de seção #

O texto da postagem pode ser formatado usando Markdown
(veja abaixo alguns exemplos e links para saber mais).

## Isto é um cabeçalho de subseção ##

Pode formatar o texto em *itálico* ou **negrito**.
Quebras de linha simples podem ser usadas para deixar o texto
mais legível, e não resultam em quebras de linha na página
formatada.

Deixe uma linha em branco para quebrar o parágrafo. Pode
incluir figuras seguindo o modelo abaixo, e referenciá-las
com (@fig:minha-figura). Deixe uma linha em branco acima e
abaixo da figura.

![Isto é uma figura com legenda](http://site.com/endereco/da/imagem.jpg){#fig:minha-figura}

É possível usar notas de rodapé[^minha-nota], que aparecem
como links no texto. Também é possível citar a nossa produção
bibliográfica usando o formato [@sobrenome:2020palavra].
Separe várias referências usando ponto-e-vírgula dentro dos
colchetes. Veja mais abaixo onde encontrar o código da citação.

[^minha-nota]: Isto é o texto da nota de rodapé.
```

</details>

Escreva o texto do post, formatando conforme o exemplo acima. Veja
também uma
[introdução ao Markdown para historiadores](https://programminghistorian.org/es/lecciones/introduccion-a-markdown)
e a
[referência completa da formatação possível](https://pandoc.org/MANUAL.html#pandocs-markdown).
Os códigos de citação podem ser consultados no arquivo
[`_data/biblio.yaml`](_data/biblio.yaml); eles seguem o formato
`@sobrenome:2020palavra` onde `sobrenome` é o do primeiro autor, seguido
do ano de publicação e da primeira palavra do título.
Ver mais detalhes sobre como citar referências bibliográficas mais
abaixo, em [Nova produção bibliográfica ou técnica](#nova-produção-bibliográfica-ou-técnica).

Outros recursos de
[apresentação](https://mmistakes.github.io/minimal-mistakes/docs/helpers/)
e
[formatação](https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/)
estão explicados na documentação do Template.

## Novo membro ##

### Primeiro passo ###

Incluir os dados do membro no arquivo
[`_data/authors.yaml`](data/authors.yaml) segundo o modelo abaixo. Não é
preciso preencher todos os links; apague os itens que não se aplicarem.
No campo `affiliation`, indique sempre o cargo atual em primeiro e os
demais em ordem cronológica decrescente.

<details>
<summary>Clique aqui para abrir o modelo :arrow_heading_down:</summary>

``` yaml
Pedro Paulo Palazzo de Almeida:
  name: "Pedro Paulo Palazzo de Almeida"
  familyName: "Almeida"
  givenName: "Pedro Paulo Palazzo"
  additionalName: "de" # Apagar esta linha se não houver partícula.
  # A bio indica apenas a sua vinculação ao grupo. Altere apenas
  # a última palavra da linha para indicar a sua função em andamento:
  # Líder, Pesquisador(a), Pós-doutorado, Doutorado, Mestrado
  # ou Graduação. Não apague a aspa simples (') no fim da linha.
  bio: '<i class="fa fa-graduation-cap"></i> Líder'
  # Apagar a linha abaixo se não quiser foto.
  avatar: "https://avatars3.githubusercontent.com/u/8295666"
  # Atenção: cadastre e-mail e telefone apenas se desejar que
  # eles sejam divulgados publicamente! Caso contrário, apague
  # as respectivas linhas.
  email: "palazzo@unb.br"
  telephone: "+55 61 31 07 74 49"
  links:
    # Apague os itens que não deseja publicar (apague as três
    # linhas de cada registro de uma vez!)
    # Por favor, preencha no mínimo ORCID, Lattes e DGP.
  - label: "ORCID"
    icon : "ai fa-fw ai-orcid"
    url  : "https://orcid.org/0000-0002-0187-774X"
  - label: "CV Lattes"
    icon : "ai fa-fw ai-lattes"
    url  : "http://lattes.cnpq.br/5767592881382885"
    # Use sempre a forma estática do link Lattes (é aquela que
    # aparece ao lado da sua foto, quando abrir o curriculum
    # completo).
  - label: "DGP"
    icon : "fa fa-fw fa-share-alt"
    url  : "http://dgp.cnpq.br/dgp/espelhorh/5767592881382885"
  - label: "Ciência Vitæ"
    icon : "ai fa-fw ai-ciencia-vitae"
    url  : "https://www.cienciavitae.pt//pt/D91E-0C60-B56B"
  - label: "OSF"
    icon : "ai fa-fw ai-osf"
    url  : "https://osf.io/79vsd/"
  - label: "Scopus"
    icon : "ai fa-fw ai-scopus"
    url  : "https://www.scopus.com/authid/detail.uri?authorId=57205888400"
  - label: "Academia.edu"
    icon : "ai fa-fw ai-academia"
    url  : "https://unb.academia.edu/PedroPalazzo"
  - label: "Google Acadêmico"
    icon : "ai fa-fw ai-google-scholar"
    url  : "https://scholar.google.com/citations?user=1C-lad4AAAAJ"
  - label: "ResearcherID"
    icon : "ai fa-fw ai-researcherid"
    url  : "https://publons.com/researcher/3774715/pedro-paulo-palazzo/"
  - label: "ResearchGate"
    icon : "ai fa-fw ai-researchgate"
    url  : "https://www.researchgate.net/profile/Pedro-Palazzo"
  - label: "Zotero"
    icon : "ai fa-fw ai-zotero"
    url  : "https://www.zotero.org/palazzo/library"
  - label: "GitHub"
    icon : "fab fa-fw fa-github"
    url  : "https://github.com/p3palazzo"
  - label: "Instagram"
    icon : "fab fa-fw fa-instagram"
    url  : "https://instagram.com/p3palazzo"
  - label: "LinkedIn"
    icon : "fab fa-fw fa-linkedin"
    url  : "https://linkedin.com/in/p3palazzo"
  - label: "Pinterest"
    icon : "fab fa-fw fa-pinterest"
    url  : "https://pinterest.com/p3palazzo"
  - label: "Twitter"
    icon : "fab fa-fw fa-twitter"
    url  : "https://twitter.com/p3palazzo"
  - label: "YouTube"
    icon : "fab fa-fw fa-youtube"
    url  : "https://youtube.com/PedroPauloPalazzo"
  - label: "Site pessoal"
    icon : "fa fa-fw fa-external-link-alt"
    url  : "https://palazzo.arq.br"
  - label: "+55 61 31 07 74 49"
    icon : "fas fa-fw fa-phone-square-alt"
    url  : "tel:+5561-3107-7449"
```

</details>

Observe a indentação de cada linha com dois ou quatro espaços. Na
dúvida, copie e cole o modelo acima, e então edite os campos
apropriados. Para incluir links não listados acima, veja os ícones
disponíveis em [Academicons](http://jpswalsh.github.io/academicons/).

:warning: Lembre-se: cadastre somente as informações que você deseja que
se tornem públicas! O site será visível para o mundo todo.

### Segundo passo ###

Criar uma página no endereço [`_person/nome-da-pessoa.md`](_person/)
contendo o texto seguinte:

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` yaml
---
# O campo 'author' deve ter o nome completo idêntico ao do
# cadastro no arquivo _data/authors.yaml
author: Pedro Paulo Palazzo de Almeida
affiliation:
# Os registros sob o dicionário 'affiliation' indicam a
# vinculação a projetos de pesquisa.
- Organization: dmcpatrimonio
  Role:
  - name: Líder
    startDate: 2018-01-09
- Organization: classico-trad-ecletico
  Role:
  - name: Coordenador
    startDate: 2018-06-18
- Organization: adaptive-construction
  Role:
  - name: Coordenador
    startDate: 2020-05-05
- Organization: doctrad
  Role:
  - name: Coordenador
    startDate: 2016-09-01
    endDate: 2020-05-04
worksFor:
# Os registros do dicionário 'worksFor' se referem a
# vínculos institucionais/empregatícios relevantes.
- Organization: Universidade de Brasília
  department: Departamento de Teoria e História da Arquitetura e do Urbanismo
  Role:
  - name: Professor Adjunto
    startDate: 2015-11-30
---
```
``` markdown
Inserir aqui o resumo do CV Lattes ou outro breve texto de
apresentação da pessoa. Pode usar formatação Markdown conforme
explicado mais acima.

# Produção bibliográfica e técnica #

Listar a produção do modo que parecer mais conveniente. Por
exemplo:

1. @palazzo:2018accouplement2. Inclua comentários se quiser.
```

</details>

<!--_,-->

O nome do arquivo deve ser todo em caixa baixa, sem acentos, e com
hífens no lugar dos espaços. Assim, a página do "João Cançado d'Ors"
será `_person/joao-cancado-dors.md`. O texto do resumo pode ser
formatado usando Markdown, conforme explicado na seção [Notícias e
outras postagens](#notícias-e-outras-postagens) acima.
Ver mais detalhes sobre como citar referências bibliográficas mais
abaixo, em [Nova produção bibliográfica ou técnica](#nova-produção-bibliográfica-ou-técnica).

## Novo projeto de pesquisa ##

Criar uma página no endereço [`_project/nome-do-projeto.md`](_project/)
com o conteúdo do modelo a seguir; editar os campos conforme apropriado.

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` yaml
---
title: Clássico Tradicional Eclético
# O 'author' do projeto é o coordenador da pesquisa.
# A grafia deve ser idêntica ao nome de autor cadastrado acima.
author: Pedro Paulo Palazzo de Almeida
identifier: classico-trad-ecletico # idêntico ao nome do arquivo, sem a extensão
parentOrganization: construcao # Identificador da linha de pesquisa à qual este projeto se vincula
tags:
- Uma palavra-chave por linha
- Cada linha começa com um hífen e espaço
- Usar as palavras-chave para indicar recorte, por exemplo
- Recorte geográfico
- Recorte cronológico
- Recorte temático
- Recorte metodológico
- Não usar pontuação nas palavras-chave
startDate: 2018-06-18 # Data de início do projeto no formato aaaa-mm-dd
endDate: # Preencher somente se o projeto já foi concluído.
excerpt: >-
  Breve descrição do projeto de pesquisa.
  Esta descrição aparece no topo da página.
---
```
```markdown
Escrever uma breve descrição dos objetivos do projeto e outras
informações relevantes. Pode formatar usando Markdown. Indicar a
produção bibliográfica e técnica decorrente do projeto, organizando do
modo que for mais relevante. Por exemplo:

# Produção bibliográfica e técnica #

## Artigos Qualis A ou internacionais ##

1. @palazzo:2020literary32. Qualis B2 Internacional

## Outros artigos ##

1. @almeida:2019luz
2. @almeida:2021papel
3. @nascimento:2019imagens13
4. @oliveira:2019avenida1
5. @oliveira:2019elementos
6. @palazzo:2020relacoes
7. @pimentellopes:2017especulacao
8. @pimentellopes:2018bases

## Outra produção bibliográfica ##

1. @ficher:2019mello
2. @palazzo:2018tipologia
3. @palazzo:2018accouplement2
4. @palazzo:2017missing
5. @palazzo:2019imagem
6. @solorzano:2019relacoes

## Produção técnica ##

1. @palazzo:2019saberes
2. @palazzo:2020teoria

## Teses e dissertações defendidas ##

1. @bercott:2019historia
2. @lima:2018narrativas
3. @pereira:2020arquitetura
4. @pimentellopes:2018natividade
5. @solorzano:2020superquadra
```

</details>

O código da linha de pesquisa é o campo `identifier` na respectiva
página, localizada na pasta [`_organization`](_organization/).
Ver mais detalhes sobre como citar referências bibliográficas mais
abaixo, em [Nova produção bibliográfica ou técnica](#nova-produção-bibliográfica-ou-técnica).

## Nova produção bibliográfica ou técnica ##

> :warning: A definir como vamos colaborar no cadastramento de
> bibliografia: Mendeley ou Zotero? Manualmente?

A produção bibliográfica do grupo está cadastrada em
[`_data/biblio.yaml`](_data/biblio.yaml). Você pode citar qualquer
referência cadastrada digitando `@` seguido do *id* da referência, que
está na forma  `sobrenome do primeiro autor:` seguido do `ano` de
publicação, a `primeira palavra do título` e eventualmente o volume da
obra. Por exemplo:

> Sarah da Silva Almeida, Valéria Ribeiro da Silva Franklin Almeida, e
> Eduardo Barbosa Lusa “Luz, câmera, preservação! O papel do cinema na
> conservação da arquitetura moderna”, in *Anais do 3º Simpósio
> Científico do ICOMOS Brasil* (3º Simpósio Científico do ICOMOS Brasil,
> Belo Horizonte: IEDS, 2019),
> https://even3.com.br/anais/iiisimposioicomosbrasil/155778-luz-camera-preservacao-o-papel-do-cinema-na-conservacao-da-arquitetura-moderna.

Deve ser citado como: `@almeida:2019luz`. A referência completa e
formatada aparecerá no mesmo lugar em que o *id* foi inserido.

* * * *

Documentação, Modelagem e Conservação do Patrimônio (c) 2020 by
pesquisadores do grupo conforme espelho oficial no
[Diretório dos Grupos de Pesquisa do CNPq](http://dgp.cnpq.br/dgp/espelhogrupo/0050065016863402)
 
Documentação, Modelagem e Conservação do Patrimônio is licensed under a
Creative Commons Attribution-ShareAlike 3.0 Unported License.
 
You should have received a copy of the license along with this
work.  If not, see <http://creativecommons.org/licenses/by-sa/3.0/>.

