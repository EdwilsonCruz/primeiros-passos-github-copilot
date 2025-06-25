## Etapa 2: Realizando tarefas com o Copilot

Na etapa anterior, o GitHub Copilot nos ajudou a conhecer o projeto. Só isso já economiza muito tempo, mas agora vamos colocar a mão na massa!

Recentemente, descobrimos que há um bug onde estudantes conseguem se inscrever duas vezes na mesma atividade. Isso não é aceitável, então vamos corrigir!

Infelizmente, recebemos poucas informações para resolver esse problema. Então, vamos pedir ajuda ao Copilot para encontrar a área problemática e sugerir uma solução.

Mas antes, vamos aprender um pouco mais sobre o Copilot! 🧑‍🚀

### Como o Copilot funciona?

Resumidamente, você pode pensar no Copilot como um colega de trabalho muito especializado. Para ser eficaz, você precisa fornecer contexto (background) e instruções claras (prompts). Além disso, pessoas diferentes são melhores em coisas diferentes por causa de suas experiências únicas (modelos).

- **Como fornecemos contexto?:** No nosso ambiente de codificação, o Copilot considera automaticamente o código próximo e as abas abertas. Se você estiver usando o chat, também pode referenciar arquivos explicitamente.

- **Qual modelo devemos escolher?:** Para este exercício, não faz muita diferença. Experimentar modelos diferentes faz parte da diversão! Isso é assunto para outra lição! 🤖

- **Como faço prompts?:** Ser explícito e claro ajuda o Copilot a fazer o melhor trabalho. Mas, diferente de sistemas tradicionais, você sempre pode esclarecer sua instrução com prompts de acompanhamento.

> [!TIP]
> Existem várias outras formas de complementar o conhecimento e as capacidades do Copilot, como [participantes de chat](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/github-copilot-chat-cheat-sheet?tool=vscode#chat-participants), [variáveis de chat](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/github-copilot-chat-cheat-sheet?tool=vscode#chat-variables), [comandos de barra](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/github-copilot-chat-cheat-sheet?tool=vscode#slash-commands-1) e [ferramentas MCP](https://code.visualstudio.com/docs/copilot/chat/mcp-servers).

### :keyboard: Atividade: Use o Copilot para corrigir o bug de inscrição :bug:

1. Vamos pedir ao Copilot para sugerir de onde pode estar vindo o bug. Abra o painel **Copilot Chat** no **modo Pergunta** e pergunte:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > @workspace Estudantes conseguem se inscrever duas vezes em uma atividade.
   > De onde pode estar vindo esse bug?
   > ```

   <details>
   <summary>O que é @workspace?</summary>

   Ótima pergunta! Este é um [participante de chat](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/github-copilot-chat-cheat-sheet?tool=vscode#chat-participants) especializado que explora o repositório do projeto e tenta incluir contexto adicional relevante.

   </details>

1. Agora que sabemos que o problema está no arquivo `src/app.py` e no método `signup_for_activity`, vamos seguir a recomendação do Copilot e corrigir (semi-manualmente). Comece com um comentário e deixe o Copilot sugerir a correção.

   1. No VS Code, selecione a aba **Explorer** para mostrar os arquivos do projeto e abra o arquivo `src/app.py`.

   1. Role até perto do final do arquivo e encontre o método `signup_for_activity`.

   1. Encontre a linha de comentário que descreve a adição de um estudante. Acima disso, é o local lógico para fazer a verificação de inscrição.

   1. Digite o comentário abaixo e pressione enter para ir para a próxima linha. Após um momento, aparecerá um texto sombreado com uma sugestão do Copilot! Legal! :tada:

      ```python
      # Validar se o estudante já está inscrito
      ```

   1. Pressione `Tab` para aceitar a sugestão do Copilot e transformar o texto sombreado em código.

      > **Dica:** Se quiser ver outras sugestões, em vez de pressionar `Tab`, passe o mouse sobre a sugestão e use as setas ou clique nos três pontos `...` e em `Open Completions Panel` para ver todas as sugestões em um painel dedicado.

   <details>
   <summary>Exemplo de resultado</summary><br/>

   O Copilot está evoluindo a cada dia e pode não produzir sempre os mesmos resultados. Se não gostar das sugestões, aqui está um exemplo válido que produzimos durante a criação deste exercício. Você pode usá-lo para continuar:

   ```python
   @app.post("/activities/{activity_name}/signup")
   def signup_for_activity(activity_name: str, email: str):
      """Sign up a student for an activity"""
      # Validate activity exists
      if activity_name not in activities:
         raise HTTPException(status_code=404, detail="Activity not found")

      # Get the specificy activity
      activity = activities[activity_name]

      # Validar se o estudante já está inscrito
      if email in activity["participants"]:
         raise HTTPException(status_code=400, detail="Already signed up")
      
      # Add student
      activity["participants"].append(email)
      return {"message": f"Signed up {email} for {activity_name}"}
   ```

   </details>

### :keyboard: Atividade: Deixe o Copilot gerar dados de exemplo 📋

Em novos projetos, é útil ter dados fictícios realistas para testes. O Copilot é excelente nisso, então vamos adicionar mais atividades de exemplo e apresentar outra forma de interagir com o Copilot usando o **Chat Inline**.

O **Chat Inline** e o painel **Copilot Chat** são ferramentas muito parecidas, mas com contexto automático um pouco diferente. Assim, enquanto o Copilot Chat é bom para explicar sobre o projeto, o chat inline pode ser mais natural para perguntar sobre uma linha ou função específica.

1. Se ainda não estiver aberto, abra o arquivo `src/app.py`.

1. Perto do topo (por volta da linha 23), encontre a variável `activities`, onde estão configuradas as atividades extracurriculares de exemplo.

1. Clique em qualquer uma dessas linhas e abra o chat inline do Copilot usando o comando de teclado `Ctrl + I` (windows) ou `Cmd + I` (mac).

   > **Dica:** Outra forma de abrir o chat inline é: clique com o botão direito em uma das linhas selecionadas -> `Copilot` -> `Editor Inline Chat`.

1. Digite o seguinte prompt e pressione enter ou o botão **Send and Dispatch**.

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > Adicione mais 2 atividades esportivas, 2 artísticas e 2 intelectuais.
   > ```

1. Após um momento, o Copilot começará a fazer alterações diretamente no código. As mudanças terão um estilo diferente para facilitar a identificação. Analise e pressione **Accept** para aceitar.

   <details>
   <summary>Exemplo de resultado</summary><br/>

   O Copilot está evoluindo a cada dia e pode não produzir sempre os mesmos resultados. Se não gostar das sugestões, aqui está um exemplo que produzimos durante a criação deste exercício. Use se tiver dificuldades.

   ```python
    "Clube de Xadrez": {
        "description": "Aprenda estratégias e participe de torneios de xadrez",
        "schedule": "Sextas, 15h30 - 17h",
        "max_participants": 12,
        "participants": ["michael@mergington.edu", "daniel@mergington.edu"]
    },
    "Aula de Programação": {
        "description": "Aprenda fundamentos de programação e desenvolva projetos de software",
        "schedule": "Terças e quintas, 15h30 - 16h30",
        "max_participants": 20,
        "participants": ["emma@mergington.edu", "sophia@mergington.edu"]
    },
    "Educação Física": {
        "description": "Educação física e atividades esportivas",
        "schedule": "Segundas, quartas e sextas, 14h - 15h",
        "max_participants": 30,
        "participants": ["john@mergington.edu", "olivia@mergington.edu"]
    },
    # Esportivas
    "Futebol": {
        "description": "Participe do time de futebol da escola e jogue campeonatos",
        "schedule": "Terças e quintas, 16h - 17h30",
        "max_participants": 22,
        "participants": ["lucas@mergington.edu", "marcos@mergington.edu"]
    },
    "Vôlei": {
        "description": "Aulas e treinos de vôlei para todos os níveis",
        "schedule": "Quartas e sextas, 15h - 16h30",
        "max_participants": 18,
        "participants": ["ana@mergington.edu", "carla@mergington.edu"]
    },
    # Artísticas
    "Teatro": {
        "description": "Oficina de teatro com apresentações semestrais",
        "schedule": "Segundas e quartas, 16h - 17h30",
        "max_participants": 15,
        "participants": ["bruno@mergington.edu", "lara@mergington.edu"]
    },
    "Clube de Música": {
        "description": "Aprenda instrumentos e participe da banda escolar",
        "schedule": "Sextas, 14h - 15h30",
        "max_participants": 12,
        "participants": ["rafael@mergington.edu", "juliana@mergington.edu"]
    },
    # Intelectuais
    "Olimpíada de Matemática": {
        "description": "Prepare-se para olimpíadas de matemática com aulas e desafios",
        "schedule": "Terças, 17h - 18h",
        "max_participants": 25,
        "participants": ["paulo@mergington.edu", "camila@mergington.edu"]
    },
    "Clube de Leitura": {
        "description": "Leitura e discussão de livros clássicos e contemporâneos",
        "schedule": "Quintas, 16h - 17h",
        "max_participants": 20,
        "participants": ["aline@mergington.edu", "fernando@mergington.edu"]
    }
   ```

   </details>

### :keyboard: Atividade: Use o Copilot para descrever nosso trabalho 💬

Ótimo trabalho corrigindo o bug e expandindo as atividades de exemplo! Agora vamos commitar e enviar para o GitHub, novamente com a ajuda do Copilot!

1. Na barra lateral esquerda, selecione a aba `Source Control`.

   > **Dica:** Abrir um arquivo pela área de controle de versão mostra as diferenças para o original, em vez de apenas abrir o arquivo normalmente.

1. Encontre o arquivo `app.py` e pressione o sinal de `+` para adicionar suas alterações à área de staging.

   ![image](https://github.com/user-attachments/assets/7d3daf4e-4125-4775-88a7-33251cd7293e)

1. Acima da lista de alterações staged, encontre a caixa de texto **Message**, mas **não digite nada** por enquanto.

   - Normalmente, você escreveria uma breve descrição das mudanças aqui, mas agora temos o Copilot para ajudar!

1. À direita da caixa **Message**, clique no botão **Generate Commit Message with Copilot** (ícone de brilhos).

1. Pressione o botão **Commit** e depois **Sync Changes** para enviar suas alterações ao GitHub.

1. Aguarde um momento para a Mona conferir seu trabalho, dar feedback e compartilhar a próxima lição.

<details>
<summary>Está com problemas? 🤷</summary><br/>

Se não receber feedback, confira:

- Certifique-se de que enviou as alterações do arquivo `src/app.py` para a branch `accelerate-with-copilot`.

</details>
