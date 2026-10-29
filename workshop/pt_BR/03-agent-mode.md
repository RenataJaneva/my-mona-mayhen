<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o jogo com fluxos de trabalho agênticos

---

Nesta parte, o Copilot passa de planejador a implementador. Em vez de escrever código linha por linha, descreva o que deseja e deixe o Copilot trabalhar nos arquivos que precisam ser alterados.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Insira este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Retorne o Copilot CLI ao fluxo normal de programação (ou continue no modo autopilot se quiser que ele prossiga até você pará-lo).
2. Se ajudar, indique o arquivo da página para dar mais contexto: `@src/pages/index.astro`.
3. Insira este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript do lado do cliente à página de batalha para que:
   > 1. Ao clicar no botão Battle, obtenha dos campos os dois nomes de usuário.
   > 2. Valide se ambos foram preenchidos e exiba um erro se algum estiver vazio.
   > 3. Busque em paralelo, pela nossa API, os dados de contribuições dos dois usuários.
   > 4. Renderize os gráficos de contribuições em grades coloridas — cada dia deve aparecer como um quadrado colorido da paleta do GitHub.
   > 5. Exiba um selo VS entre os dois usuários.
   > 6. Mostre o nome de usuário, o total de contribuições e o intervalo de datas de cada pessoa.
   > 7. Trate os estados de carregamento e os erros.
   > 8. Dispare a batalha também ao pressionar Enter nos campos de entrada.
   > 9. Mantenha a interface simples, conforme a estrutura inicial já criada.
   >
   > Use interfaces do TypeScript para a estrutura dos dados de contribuições.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI implementar as alterações em `src/pages/index.astro`.
5. Use `/diff` para revisar as alterações geradas e depois aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não tiver sido atualizada, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador.

1. Digite `octocat` e `torvalds` como os dois nomes de usuário e clique em **Battle**.
2. Você deve ver os gráficos de contribuições dos dois usuários lado a lado, em grades coloridas.
3. Teste os casos de erro:
   - Deixe um ou os dois campos vazios e clique em Battle — deve aparecer um erro de validação.
   - Digite um nome de usuário inválido — o aplicativo deve exibir um erro da API.
4. Pressione **Enter** em qualquer campo de entrada — a batalha deve ser iniciada como se você tivesse clicado no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver certo, envie comentários diretamente ao Copilot. Por exemplo:

- *"Os quadrados de contribuições estão grandes demais; ajuste-os para 12x12 px"*
- *"Adicione uma dica ao passar o cursor mostrando a data e a contagem de contribuições"*
- *"O estado de carregamento precisa de uma animação pulsante"*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e iterações. Cada prompt de acompanhamento aproveita o contexto da conversa anterior, permitindo refinar a implementação aos poucos sem começar do zero.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento aproveita o anterior. Use `/session` ou `/context` para inspecionar o contexto que o Copilot está mantendo e `/review` depois de uma iteração maior para procurar bugs ou melhorias.
<!-- track:cli:end -->

## Dicas para esta parte

- **Seja específico sobre o que deseja** — requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las** — inspecionar o código gerado é mais rápido do que reescrevê-lo depois.
- **Teste o aplicativo após cada etapa de implementação** para localizar os problemas.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar funcionalidades em vários arquivos**.
- **Iterar nos resultados** com comentários específicos.
- Gerenciar o **ciclo completo de uma funcionalidade** — implementação, revisão, testes e refinamento.
