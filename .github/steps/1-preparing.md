## Etapa 1: Oi Copilot

Bem-vindo ao seu exercício de **"Primeiros Passos com o GitHub Copilot"**! :robot:

Neste exercício, você usará diferentes recursos do GitHub Copilot para trabalhar em um site que permite aos alunos da Escola Mergington High se inscreverem em atividades extracurriculares. 🎻 ⚽️ ♟️

<img width="600" alt="screenshot do WebApp da Escola Mergington High" src="https://github.com/user-attachments/assets/472398fd-1aa1-4084-b443-4e242deb30d9" />

### O que é o GitHub Copilot?

<img width="150" align="right" alt="logo do copilot" src="https://github.com/user-attachments/assets/4d22496d-850b-4785-aafe-11cba03cd5f2" />

O GitHub Copilot é um assistente de codificação com IA que ajuda você a escrever código mais rápido e com menos esforço, permitindo que você concentre mais energia na resolução de problemas e na colaboração.

O GitHub Copilot comprovadamente aumenta a produtividade do desenvolvedor e acelera o ritmo do desenvolvimento de software. Para mais informações, veja [Pesquisa: quantificando o impacto do GitHub Copilot na produtividade e felicidade do desenvolvedor no blog do GitHub.](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/)


Suas interações mais comuns provavelmente serão:

- **Sugestões em linha**: Enquanto você digita, o Copilot usa o contexto próximo para sugerir código diretamente no seu editor. Esta será uma interação familiar se você já usou ferramentas de sugestão de código como o [Intellisense](https://code.visualstudio.com/docs/editor/intellisense), exceto que as completações podem ser funções inteiras.

- **Copilot - Modo Pergunta (Ask)**: Um painel de chat dedicado que permite fazer perguntas relacionadas à codificação. Isso parecerá familiar se você já usou chats de assistentes de IA online. A grande diferença, no entanto, é que seus arquivos de projeto fornecerão contexto automático para fornecer respostas personalizadas.

- **Copilot - Modo Edição(Edit)**: Similar ao modo Pergunta, mas menos conversacional. O Copilot fará alterações nos seus arquivos selecionados para implementar sua solicitação.

- **Copilot - Modo Agente(Agent)**: O Copilot será executado iterativamente até atingir sua solicitação. Ele selecionará contexto, fará alterações no código, executará comandos de terminal, ferramentas e, o mais importante, revisará seu trabalho para fazer ajustes.

> [!TIP]
> Você pode aprender mais sobre recursos atuais e futuros na documentação de [Recursos do GitHub Copilot](https://docs.github.com/en/copilot/about-github-copilot/github-copilot-features). Você também pode selecionar diferentes [modelos](https://docs.github.com/en/github-models) e criar suas próprias [extensões](https://github.com/features/copilot/extensions), mas isso é assunto para outra lição!

### Como posso usar o GitHub Copilot?

Ao trabalhar, você descobrirá que o GitHub Copilot pode ajudar em vários lugares no site do GitHub e em suas IDEs de codificação favoritas, como VS Code, Visual Studio,Jet Brains e Xcode! 

### :keyboard: Atividade: Configurando o ambiente
Para a codificação de hoje, porém,  precisaremos de escolher como executar nossa aplicação.

<details>
<summary>Configurando o Codespaces</summary><br/>

Vamos iniciar nosso ambiente de desenvolvimento pré-configurado conhecido como [Codespace](https://github.com/features/codespaces), usar o Copilot para aprender um pouco sobre o projeto e depois testá-lo.

1. Clique com o botão esquerdo no botão abaixo para abrir a página **Criar Codespace** em uma nova aba. Use a configuração padrão.

   [![Abrir no GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. Confirme que o campo **Repository** é sua cópia do exercício, não o original, e depois clique no botão verde **Create Codespace**.

   - ✅ Sua cópia: `/{{{full_repo_name}}}`
   - ❌ Original: `/dev-pods/primeiros-passos-github-copilot`

1. Aguarde um momento para que o Visual Studio Code carregue no seu navegador.

</details>

<details>
<summary>Configurando o ambiente local</summary><br/>
Para configurar o ambiente local, vamos precisar de instalar e configurar alguns pré requisitos:

- [Python 3](https://www.python.org/downloads/)
- [VSCODE](https://code.visualstudio.com/)
   - Com as seguintes extensões:
      - GitHub.copilot
      - ms-python.python
      - ms-python.debugpy


</details>


### :keyboard: Atividade: Obtenha uma introdução ao projeto do Copilot Chat

1. Na barra lateral esquerda, clique na aba de extensões e verifique se as extensões `GitHub Copilot` e `Python` estão instaladas e ativadas.

   <img width="350" alt="extensão do copilot para VS Code" src="https://github.com/user-attachments/assets/ef1ef984-17fc-4b20-a9a6-65a866def468" />

   <img width="350" alt="extensão python para VS Code" src="https://github.com/user-attachments/assets/3040c0f5-1658-47e2-a439-20504a384f77" />

1. Na parte superior do VS Code, localize e clique no **ícone do Copilot** para abrir um painel de Chat do Copilot.

   <img width="150" alt="imagem" src="https://github.com/user-attachments/assets/5e64db46-95cb-415d-badc-b6b8677f10c1" />

1. Se esta é a primeira vez que você usa o GitHub Copilot, precisará aceitar os termos de uso para continuar.

1. Digite o prompt abaixo para pedir ao Copilot que apresente o projeto a você.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > @workspace Por favor, explique brevemente a estrutura deste projeto.
   > O que devo fazer para executá-lo?
   > ```

   > **Observação**: Não é necessário seguir as instruções recomendadas pelo Copilot. Já preparamos o ambiente para você.

   <details>
   <summary>O que é @workspace?</summary>
   Bom trabalho notando os detalhes, mas vamos apenas usá-lo por enquanto. 🤓 Prometemos explicar no próximo passo.
   </details>

1. Agora que sabemos um pouco mais sobre o projeto, vamos realmente tentar executá-lo! Na barra lateral esquerda, selecione a aba `Executar e Depurar` e pressione o ícone **Iniciar Depuração**.

   <img width="300" alt="imagem" src="https://github.com/user-attachments/assets/50b27f2a-5eab-4827-9343-ab5bce62357e" />

1. Queremos ver nossa página web executando em um navegador, então vamos encontrar a URL e a porta. Se não estiver visível, expanda o painel inferior e selecione a aba **Portas**.

1. Na lista, encontre a porta `8000` e o link relacionado. Passe o mouse sobre o link e selecione o ícone **Abrir no navegador**.

   ![imagem](https://github.com/user-attachments/assets/92d5642e-ce99-4a66-850c-2d311a673596)

### :keyboard: Atividade: Use o Copilot para ajudar a lembrar de um comando de terminal 🙋

Ótimo trabalho! Agora que estamos familiarizados com o aplicativo e sabemos que ele funciona, vamos pedir ajuda ao Copilot para iniciar uma branch para que possamos fazer algumas personalizações.

1. Se ainda não estiver lá, retorne ao VS Code.

1. No painel inferior, selecione a aba **Terminal**. No lado direito, clique no sinal de mais `+` para criar uma nova janela de terminal.

   > **Observação:** Isso evitará interromper a sessão de depuração existente que está hospedando nosso serviço de aplicativo web.

1. Na nova janela do terminal, use o atalho de teclado `Ctrl + I` (windows) ou `Cmd + I` (mac) para abrir o **Chat em Linha do Terminal do Copilot**.

1. Vamos pedir ao Copilot que nos ajude a lembrar de um comando que esquecemos: criar uma branch e publicá-la.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Ei copilot, como posso criar e publicar uma nova branch do Git?
   > ```

   > **Dica:** Este é um exemplo simples, mas o Copilot é ótimo para fornecer comandos mais personalizados que podem envolver loops, correspondência de padrões, modificação de arquivos e muito mais! Não tenha medo de pedir uma sugestão ao Copilot. Apenas lembre-se de que é uma sugestão e você sempre deve verificá-la primeiro para garantir segurança.

1. O Copilot provavelmente nos deu um comando como o seguinte. Em vez de modificá-lo manualmente, vamos responder para informar ao Copilot que use um nome específico.

   ```bash
   git checkout -b {novo_nome_da_branch}
   git push -u origin {novo_nome_da_branch}
   ```

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Incrível! Obrigado, Copilot! Vamos usar o nome de branch "accelerate-with-copilot".
   > ```

   > **Dica:** Se o Copilot não lhe der exatamente o que você deseja, você sempre pode continuar explicando o que precisa. O Copilot lembrará do histórico da conversa para respostas de acompanhamento.

1. Agora que estamos satisfeitos com o comando, pressione o botão `Executar` para deixar o Copilot executá-lo para nós. Não é necessário copiar e colar!

1. Depois de um momento, olhe na barra de status inferior do VS Code, à esquerda, para ver a branch ativa. Deve agora dizer `accelerate-with-copilot`. Se sim, você concluiu esta etapa!

1. Agora que sua branch foi enviada para o GitHub, Mona já deve estar ocupada verificando seu trabalho. Dê a ela um momento e fique atento nos comentários. Você verá ela responder com informações de progresso e a próxima lição.

<details>
<summary>Está tendo problemas? 🤷</summary><br/>

Se você não receber feedback, aqui estão algumas coisas para verificar:

- Certifique-se de que criou a branch com o nome exato `accelerate-with-copilot`. Sem prefixos ou sufixos.
- Certifique-se de que a branch foi realmente publicada no seu repositório.

</details>
