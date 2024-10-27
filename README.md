# Definição
Mensageria é o conceito que possibilita a comunicação entre sistemas distribuídos por meio da troca de mensagens (ou eventos), com essas mensagens sendo intermediadas por um Message Broker (servidor ou módulo de mensageria). Esse mecanismo permite que os sistemas interajam de forma assíncrona, ou seja, sem a necessidade de aguardarem uma resposta imediata.

# Definição simplificada:
Diferente do modelo síncrono usado em requisições HTTP, onde a resposta é aguardada para continuar o processamento, a mensageria permite que a comunicação entre sistemas ocorra de maneira assíncrona. Isso significa que o sistema emissor envia uma mensagem e pode continuar suas operações sem precisar esperar pela resposta do receptor.

# Exemplo:
Considere dois sistemas, o Sistema A e o Sistema B. O Sistema A deseja enviar um e-mail. Em vez de realizar o envio diretamente e esperar que o Sistema B complete a tarefa, o Sistema A cria uma mensagem com a solicitação ("enviar e-mail com o conteúdo X") e a entrega para o Message Broker.

O Message Broker se encarrega de passar essa mensagem para o Sistema B, que, por sua vez, processará o envio do e-mail no momento adequado. Caso ocorra um problema no envio, a mensagem pode ser reenviada ou tratada posteriormente, sem impactar o funcionamento do Sistema A, que já seguiu seu fluxo de trabalho normalmente após entregar a mensagem.

# Vantagens:
- Assincronia: O sistema que envia a mensagem não precisa parar para aguardar o processamento da tarefa.
- Desacoplamento: Sistemas emissores e receptores podem funcionar independentemente, sem precisar de conexão direta ou sincronização.
- Escalabilidade: O uso de mensageria facilita a distribuição de tarefas entre diferentes sistemas, permitindo que elas sejam executadas em paralelo ou em momentos distintos, conforme a disponibilidade do sistema receptor.
