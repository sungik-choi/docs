---
title: Sobre pull requests
intro: 'As pull requests permitem que você informe outras pessoas sobre as alterações das quais você fez push para um branch em um repositório no {% data variables.product.product_name %}. Depois que uma pull request é aberta, você pode discutir e revisar as possíveis alterações com colaboradores e adicionar commits de acompanhamento antes que as alterações sofram merge no branch base.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
  - /articles/using-pull-requests
  - /articles/about-pull-requests
  - /github/collaborating-with-issues-and-pull-requests/about-pull-requests
  - /github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

## Sobre pull requests

{% note %}

**Observação:** ao trabalhar com pull requests, lembre-se do seguinte:
* Se estiver trabalhando no [modo de repositório compartilhado](/pull-requests/collaborating-with-pull-requests/getting-started/about-collaborative-development-models), é recomendável usar um branch de tópico para sua pull request. Embora você possa enviar pull requests de qualquer branch ou commit, com um branch de tópico, é possível fazer push de commits de acompanhamento caso seja preciso atualizar as alterações propostas.
* Tenha muito cuidado quando fizer push forçado de commits para um pull request. Faz push forçado das alterações no histórico do repositório e pode corromper o seu pull request. Se outros colaboradores fizerem o branch do projeto antes de um push forçado, este poderá substituir os commits nos quais os colaboradores basearam o seu trabalho.

{% endnote %}

Você pode criar pull requests no {% data variables.product.prodname_dotcom_the_website %}, com {% data variables.product.prodname_desktop %}, em {% data variables.product.prodname_github_codespaces %}, em {% data variables.product.prodname_mobile %} e ao usar a CLI do GitHub.

Após inicialização de uma pull request, você verá uma página de revisão que mostra uma visão geral de alto nível das alterações entre seu branch (o branch de comparação) e o branch base do repositório. É possível adicionar um resumo das alterações propostas, revisar as alterações feitas pelos commits, adicionar etiquetas, marcos e responsáveis, bem como fazer @menção a contribuidores individuais ou equipes. Para obter mais informações, consulte "[Criar uma pull request](/articles/creating-a-pull-request)".

Depois que tiver criado uma pull request, você poderá fazer push dos commits do branch de tópico para adicioná-los à sua pull request existente. Esses commits aparecerão em ordem cronológica na pull request e as alterações estarão visíveis na guia "Files chenged" (Arquivos alterados).

Outros contribuidores podem revisar as alterações propostas, adicionar comentários de revisão, contribuir com a discussão da pull request e, até mesmo, adicionar commits à pull request. {% ifversion pull-request-approval-limit %}{% data reusables.pull_requests.code-review-limits %}{% endif %}

{% ifversion fpt or ghec %}
Você pode ver as informações sobre o status da implantação atual do branch e atividades passadas de implantação na guia "Conversa". Para obter mais informações, consulte "[Exibir atividade de implantação para um repositório](/repositories/viewing-activity-and-data-for-your-repository/viewing-deployment-activity-for-your-repository)".
{% endif %}

Quando estiver satisfeito com as alterações propostas, você poderá fazer merge da pull request. Se você está trabalhando em um modelo de repositório compartilhado, você cria uma pull request e, você ou outra pessoa, fará a mesclagem de suas alterações do seu branch de recurso no branch base que você especificar na sua pull request. Para obter mais informações, consulte "[Fazer merge de uma pull request](/articles/merging-a-pull-request)".

{% data reusables.pull_requests.required-checks-must-pass-to-merge %}

{% data reusables.pull_requests.close-issues-using-keywords %}

{% tip %}

**Dicas:**
- Para alternar entre as opções de recolhimento e expansão de todos os comentários de revisão desatualizados em uma pull request, mantenha pressionados <span class="platform-mac"><kbd>opção</kbd></span><span class="platform-linux"><kbd>Alt</kbd></span><span class="platform-windows"><kbd>Alt</kbd></span> e clique em **Mostrar desatualizados** ou **Ocultar desatualizados**. Para ver mais atalhos, consulte "[Atalhos de teclado](/articles/keyboard-shortcuts)".
- Você pode combinar commits por squash ao fazer merge de uma pull request para obter uma exibição mais simplificada das alterações. Para obter mais informações, consulte "[Sobre merges da pull request](/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges)".

{% endtip %}

É possível acessar seu painel a fim de encontrar rapidamente links para pull requests recentemente atualizadas nas quais você está trabalhando ou nas quais está inscrito. Para obter mais informações, consulte "[Sobre seu painel pessoal](/articles/about-your-personal-dashboard)".

## Pull requests de rascunho

{% data reusables.gated-features.draft-prs %}

Ao criar uma pull request, você pode optar por criar uma que já está pronta para revisão ou uma pull request de rascunho. Não é possível fazer merge das pull requests, e os proprietários do código não são solicitados automaticamente a revisar pull requests de rascunho. Para obter mais informações sobre como criar uma pull request de rascunho, consulte "[Criar uma pull request](/articles/creating-a-pull-request)" e "[Criar uma pull request de uma bifurcação](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)".

{% data reusables.pull_requests.mark-ready-review %} Você pode converter uma pull request em rascunho a qualquer momento. Para obter mais informações, consulte "[Alterar o stage de um pull request](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/changing-the-stage-of-a-pull-request)".

## Diferenças entre commits em páginas de comparação e pull request

As páginas de comparação e pull request usam métodos diferentes para calcular o diff para os arquivos alterados:

- As páginas de comparação mostram a diferença entre a ponta do ref principal e o ancestral comum atual (ou seja, a base de merge) do ref principal e de base.
- As páginas de pull request mostram a diferença entre a ponta do ref principal e o ancestral comum do ref principal e de base no momento em que o pull request foi criado. Consequentemente, a base de merge utilizada para a comparação pode ser diferente.

## Leia mais

- "[pull request](/articles/github-glossary/#pull-request)" no glossário do {% data variables.product.prodname_dotcom %}
- "[Sobre branches](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches)"
- "[Comentando em uma pull request](/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request)"
- "[Fechar uma pull request](/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/closing-a-pull-request)"
