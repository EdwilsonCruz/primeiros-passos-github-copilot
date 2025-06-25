## Etapa 3: Trabalhando ainda _mais rápido_ com Copilot Edits

Nas etapas anteriores, usamos recursos do Copilot que exigem mais orientação manual e produzem resultados mais localizados. Agora, vamos explorar o Copilot Edits, um recurso que permite trabalhar de forma mais holística no nosso repositório.

[Copilot - Modo Edição](https://code.visualstudio.com/docs/copilot/copilot-edits) é uma sessão de edição de código com IA para fazer alterações em **múltiplos arquivos** usando **linguagem natural**, aplicando as edições diretamente no editor, onde você pode revisá-las no contexto completo do código ao redor.

#### Principais recursos

- **Edição em múltiplos arquivos**: O Copilot Edits pode fazer alterações em vários arquivos do seu workspace.
- **Fluxo iterativo**: Projetado para iteração rápida, permitindo revisar, aceitar ou descartar o código gerado pela IA.
- **Edição no local**: Mostra o código gerado diretamente no seu editor, proporcionando um fluxo semelhante a uma revisão de código.
- **Conjunto de trabalho**: Permite definir em quais arquivos as edições devem ser aplicadas.

#### Como funciona

1. **Defina o contexto**: Selecione os arquivos que farão parte do conjunto de trabalho.
1. **Forneça instruções**: Use linguagem natural para descrever as mudanças necessárias.
1. **Revise as alterações**: Veja as alterações propostas diretamente no seu código.
1. **Aceite ou descarte**: Revise cada sugestão e escolha quais manter.
1. **Itere**: Se necessário, forneça instruções adicionais para refinar as mudanças.

### :keyboard: Atividade: Use o Copilot para adicionar uma nova funcionalidade! :rocket:

1. Se o painel do Copilot Chat não estiver visível, reabra-o.

1. Na parte inferior da janela do Copilot Chat, use o menu suspenso para trocar para o modo **Edição**.

   <img width="350" alt="image" src="https://github.com/user-attachments/assets/646fc94a-7d60-4821-b9cf-9ec6f4fd03d7" />

1. Abra os arquivos relacionados à nossa página web e arraste cada janela do editor (ou arquivo) para o painel de chat, informando ao Copilot para usá-los como contexto.

   - `src/static/app.js`
   - `src/static/index.html`
   - `src/static/styles.css`

   > **Dica:** Você também pode usar o botão **Add Context...** para fornecer outros itens de contexto, como uma issue do GitHub, todo o codebase ou o resultado de um terminal.

1. Peça ao Copilot para atualizar o projeto exibindo os participantes atuais das atividades. Aguarde um momento para as sugestões de edição aparecerem e serem aplicadas.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Olá Copilot, pode editar os cards de atividade para adicionar uma seção de participantes?
   > Ela deve mostrar os participantes já inscritos naquela atividade como uma lista com marcadores.
   > E lembre-se de deixar bonito!
   > ```

   - Um ícone extra aparecerá ao lado dos nomes dos arquivos e janelas abertas indicando que há sugestões de edição.
   - Um painel de sugestões de edição aparecerá no canto inferior direito do editor, com controles para navegar pelas mudanças recomendadas.

      <img width="200" alt="arquivos com ícones indicando que foram editados" src="https://github.com/user-attachments/assets/9c7c2e10-cd18-43c5-9947-cffd6dde0473" />

      <img width="250" alt="painel de navegação de edições" src="https://github.com/user-attachments/assets/a84965a5-2f43-4c93-a814-0fdeb3a06494" />

   <details>
   <summary>Precisa de ajuda? 🤷</summary><br/>

   Lembre-se de adicionar os arquivos relevantes ao conjunto de trabalho.

   ![screenshot do conjunto de trabalho](https://github.com/user-attachments/assets/d3eadc8e-583e-4a28-9e82-be128eab843b)

   </details>

1. Antes de simplesmente aceitar as mudanças, confira novamente o site e verifique se tudo foi atualizado como esperado. Aqui está um exemplo de card de atividade atualizado. Talvez seja necessário reiniciar o app ou atualizar a página.

   <img width="350" alt="Card de atividade com info de participantes" src="https://github.com/user-attachments/assets/c4d56187-4791-4c8e-87d7-d5ce7cdc0bee" />

   > **Nota:** Seu card pode estar diferente. O Copilot nem sempre gera o mesmo resultado.

   <details>
   <summary>Precisa de ajuda? 🤷</summary><br/>
   Se o site não carregar, confira:

   - Reinicie o depurador do VS Code para garantir que a versão mais recente do site está publicada.
   - Se esqueceu a URL ou fechou a janela, revise o passo 1.
   - Tente atualizar a página forçadamente ou abrir em uma janela anônima para baixar uma cópia nova.

   </details>

1. Agora que confirmamos que as mudanças estão corretas, use o painel para navegar por cada sugestão e pressione **Keep** para aplicar a alteração.

   > **Dica:** Você pode aceitar as mudanças diretamente, modificá-las ou fornecer instruções adicionais para refiná-las usando o chat.

1. Com a nova funcionalidade pronta, faça o **commit** e **push** das alterações para o GitHub.

1. Aguarde um momento para a Mona conferir seu trabalho, dar feedback e compartilhar a lição final. Quase lá!

1. (opcional) Se quiser um passo bônus não avaliado para conhecer rapidamente o modo Agente, **adicione um comentário em uma issue** perguntando ao **@professortocat** sobre o modo Copilot Agent. 🚀

   ```txt
   Olá @professortocat, o modo agente parece bem interessante. Pode me contar mais sobre ele?
   ```

<details>
<summary>Está com problemas? 🤷</summary><br/>

Se não receber feedback, confira:

- Certifique-se de que fez commit das alterações no diretório `src/static/` para a branch `accelerate-with-copilot` e enviou/sincronizou para o GitHub.
- Se a Mona encontrou algum erro, basta corrigir e enviar novamente. A Mona vai checar seu trabalho quantas vezes for preciso.

</details>
