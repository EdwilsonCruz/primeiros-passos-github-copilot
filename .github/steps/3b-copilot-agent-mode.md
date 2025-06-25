### :keyboard: Atividade Bônus - Modo Agente do GitHub Copilot

> [!NOTA]
> Esta atividade é opcional e não é avaliada.

### O que é o modo "Agente"?

O modo **Agente** aprimora o Copilot fornecendo feedback automaticamente, normalmente do tipo que você daria após revisar as edições sugeridas pelo Copilot.

O modo **Agente** dá ao Copilot um ciclo de feedback, permitindo que ele inspecione seus próprios resultados em busca de problemas, bugs, inconsistências, etc., tanto no código quanto no terminal! Isso permite que ele revise automaticamente seu trabalho em muitas situações. Da mesma forma, o modo **Agente** geralmente consegue lidar com tarefas mais complexas e de múltiplos passos.

Essa é apenas uma introdução breve e há muito mais para aprender, mas isso fica para um exercício futuro dedicado. (dica)

Agora, vamos experimentar o modo **Agente**! 👩‍🚀

### :keyboard: Atividade: Use o modo Agente para adicionar botões funcionais de "desinscrever"

Vamos experimentar solicitações mais abertas que vão adicionar mais funcionalidades ao nosso aplicativo web. Lembre-se: assistentes de IA frequentemente produzem resultados diferentes, mesmo com o mesmo prompt. Se não conseguir o resultado desejado, tente outros modelos ou forneça feedback para refinar os resultados.

1. Abra o painel de chat do **Copilot** e use o menu suspenso para trocar para o modo **Agente**.

   <img width="250" alt="image" src="https://github.com/user-attachments/assets/8c537e2a-d89a-4908-8d35-77c7f0830805" />

1. Hora do teste! Peça ao Copilot para adicionar funcionalidade de remoção de participantes.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > #codebase Por favor, adicione um ícone de deletar ao lado de cada participante e oculte os marcadores.
   > Ao clicar, deve desinscrever esse participante da atividade.
   > ```

   - Se você tentar esse prompt no modo **Edição**, provavelmente verá que as mudanças no frontend e backend foram feitas de forma teórica. Embora não ocorram erros de sintaxe ou execução, as mudanças podem não ser compatíveis e não atingir o objetivo.
   - No modo **Agente**, o Copilot revisa seu próprio trabalho e refina para garantir que todas as mudanças estejam corretas e coordenadas.

1. Quando o Copilot terminar, reinicie o depurador e inspecione os resultados. Se gostar, pressione o botão **Keep**. Caso contrário, forneça feedback ao Copilot para refinar os resultados.

1. Peça ao Copilot para corrigir um bug de registro.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > #codebase Notei que parece haver um bug.
   > Quando um participante é registrado, a página precisa ser atualizada para mostrar a mudança na atividade.
   > ```

   - Se você tentar esse prompt no modo **Edição**, pode funcionar ou não.

1. Quando o Copilot terminar, inspecione os resultados. Se gostar, pressione o botão **Keep**. Caso contrário, forneça feedback ao Copilot.

### :keyboard: Atividade: Use o modo Agente para trocar o banco de dados! 🧑‍🚀

Só por diversão, vamos tentar algo ainda mais difícil e aberto para ver o que acontece!

> [!TIP]
> Em nossos testes, conseguimos resultados funcionais na maioria das vezes, mas nem sempre.
> Você pode tentar outros modelos ou pausar para fornecer feedback ao Copilot.

1. (opcional) Se estiver disponível para você, experimente outro modelo como `Claude 3.5 Sonnet`.

   <img width="250" alt="image" src="https://github.com/user-attachments/assets/16125b88-8428-4f62-9c1b-5761e26ed888" />

1. Peça ao Copilot para instalar um serviço de banco de dados local.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Por favor, instale um servidor mongodb local para desenvolvimento.
   > Depois, execute um comando que liste as coleções para verificar se o serviço está ativo e funcionando.
   > Não modifique nosso programa ainda.
   > ```

   - O ambiente de desenvolvimento padrão foi propositalmente configurado para não estar pronto para instalar um MongoDB local.
   - Você verá o Copilot cometer erros, analisar mensagens de erro e pedir para rodar comandos extras para ajustar o ambiente. Legal!

1. Peça ao Copilot para alterar nosso app para usar o serviço de banco de dados. 🤯

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > #codebase Não gosto de armazenar os dados em memória.
   > Vamos trocar para usar mongodb.
   > Por enquanto, use a instância local de desenvolvimento.
   > Por favor, preencha o banco de dados com as atividades json já existentes, mantendo o nome da atividade como chave.
   > ```

1. Esse é só um preview por enquanto. Esperamos que tenha se divertido e volte em breve na [página de Skills](https://skills.github.com) para um exercício dedicado a explorar ainda mais o modo Agente! 🧑‍🚀 🚀
