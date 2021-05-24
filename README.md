# Documentação, Modelagem e Conservação do Patrimônio #

![Verifica estado do site](https://github.com/dmcpatrimonio/arqtrad/workflows/Website/badge.svg?branch=master)

Site do grupo de pesquisa. Usamos:

- [Jekyll](https://jekyllrb.com)
- Template [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
- [Academicons](http://jpswalsh.github.io/academicons/)

## Como atualizar este site ##

Após atualizar qualquer página, o site leva alguns minutos para ser
atualizado. Instruções específicas:

* * * *

1. [Notícias e outras postagens](#notícias-e-outras-postagens)
2. [Novo membro](#novo-membro)
3. [Novo projeto de pesquisa](#novo-projeto-de-pesquisa)
4. [Nova produção bibliográfica ou técnica](#nova-produção-bibliográfica-ou-técnica)

* * * *

### Notícias e outras postagens ###

Crie uma página no endereço
[`_posts/2021-02-28-titulo-resumido.md`](_posts/) seguindo o modelo
abaixo.

O nome do arquivo deve começar com a data no formato `aaaa-mm-dd` e na
sequência um breve nome explicativo (não precisa ser idêntico ao
título), tudo em caixa baixa e sem acentos ou espaços (use hífens para
separar os elementos e as palavras do nome). O nome do autor indicado no
topo do arquivo, este sim, precisa ser idêntico ao nome do pesquisador
tal como cadastrado no arquivo [`_data/authors.yaml`](_data/authors.yaml)
(saiba mais abaixo, na seção [Novo membro](#novo-membro)).

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` markdown
---
title: Título completo do post numa linha só
author: Nome do autor
date: 2021-02-28
---

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
do ano de publicação e da primeira palavra do título. Veja mais abaixo
como incluir novas publicações.

Outros recursos de
[apresentação](https://mmistakes.github.io/minimal-mistakes/docs/helpers/)
e
[formatação](https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/)
estão explicados na documentação do Template.

### Novo membro ###

#### Primeiro passo ####

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
  additionalName: "de" # Eliminar esta linha se não houver partícula.
  # A bio indica apenas a sua vinculação ao grupo. Altere apenas
  # a última palavra da linha para indicar a sua função em andamento:
  # Líder, Pesquisador(a), Pós-doutorado, Doutorado, Mestrado
  # ou Graduação. Não apague a aspa simples (') no fim da linha.
  bio: '<i class="fa fa-graduation-cap"></i> Líder'
  avatar: "https://avatars3.githubusercontent.com/u/8295666"
  # Atenção: cadastre e-mail e telefone apenas se desejar que
  # eles sejam divulgados publicamente! Caso contrário, apague
  # as respectivas linhas
  email: "palazzo@unb.br"
  telephone: "+55 61 31 07 74 49"
  links:
    # Apague os itens que não deseja publicar (apague as três
    # linhas de cada registro de uma vez!)
  - label: "ORCID"
    icon : "ai fa-fw ai-orcid"
    url  : "https://orcid.org/0000-0002-0187-774X"
  - label: "CV Lattes"
    icon : "ai fa-fw ai-lattes"
    url  : "http://lattes.cnpq.br/5767592881382885"
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

Observe a indentação com dois espaços. Na dúvida, copie e cole o modelo
acima, e então edite os campos apropriados. Para incluir links não
listados acima, veja os ícones disponíveis em
[Academicons](http://jpswalsh.github.io/academicons/).

:warning: Lembre-se: cadastre somente as informações que você deseja que
se tornem públicas! O site será visível para o mundo todo.

#### Segundo passo ####

Criar uma página no endereço [`_person/nome-da-pessoa.md`](_person/)
contendo o texto seguinte:

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` yaml
---
title: Pedro Paulo Palazzo de Almeida # Nome da pessoa idêntico ao do cadastro acima
author: Pedro Paulo Palazzo de Almeida # Repetir o nome idêntico
affiliation:
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
- Organization: Universidade de Brasília
  department: Departamento de Teoria e História da Arquitetura e do Urbanismo
  Role:
  - name: Professor Adjunto
    startDate: 2015-11-30
---

Inserir aqui o resumo do CV Lattes ou outro breve texto de apresentação
da pessoa.

```

</details>

<!--_,-->

O nome do arquivo deve ser todo em caixa baixa, sem acentos, e com
hífens no lugar dos espaços. Assim, a página do "João Cançado d'Ors"
será `_person/joao-cancado-dors.md`. O texto do resumo pode ser
formatado usando Markdown, conforme explicado na seção [Notícias e
outras postagens](#notícias-e-outras-postagens) acima.

### Novo projeto de pesquisa ###

Criar uma página no endereço [`_project/nome-do-projeto.md`](_project/)
com o conteúdo do modelo a seguir; editar os campos conforme apropriado.

<details>
<summary> Clique aqui para abrir o modelo :arrow_heading_down: </summary>

``` yaml
---
title: Clássico Tradicional Eclético
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
header: # Seção opcional, caso haja uma imagem representativa do projeto.
  image: "https://repository-images.githubusercontent.com/224453298/09a3bd80-60be-11ea-83cb-4b22bffcf270"
  image_description: "Foto antiga da avenida Rio Branco mostrando edifícios ecléticos"
  caption: "Foto: Augusto Malta, acervo IMS/Brasiliana Fotográfica"
  og_image: # Imagem menor, para compartilhamento em redes sociais
nocite: >- # Produção bibliográfica decorrente, separada por vírgulas
  @palazzo:2018accouplement,
  @solorzano:2019relacoes
---
```

</details>

O código da linha de pesquisa é o campo `identifier` na respectiva
página, localizada na pasta [`_organization`](_organization/).

### Nova produção bibliográfica ou técnica ###

A definir como vamos colaborar no cadastramento de bibliografia:
Mendeley ou Zotero?

* * * *

Documentação, Modelagem e Conservação do Patrimônio (c) 2020 by
pesquisadores do grupo conforme espelho oficial no
[Diretório dos Grupos de Pesquisa do CNPq](http://dgp.cnpq.br/dgp/espelhogrupo/0050065016863402)
 
Documentação, Modelagem e Conservação do Patrimônio is licensed under a
Creative Commons Attribution-ShareAlike 3.0 Unported License.
 
You should have received a copy of the license along with this
work.  If not, see <http://creativecommons.org/licenses/by-sa/3.0/>.

