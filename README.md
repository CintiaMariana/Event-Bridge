# Amazon EventBridge

**Gabriel da Silva Pereira**  
**Cintia Mariana Carvalho de Oliveira**  

**
**Curso de Sistemas de Informação**  
**Pouso Alegre – MG, 2024**

---



## O que é?

O 

O


**Amazon EventBridge** é uma evolução do **Amazon CloudWatch Events**, com maior flexibilidade e suporte para eventos personalizados de aplicativos de terceiros e serviços SaaS (Software as a Service). Ele captura, roteia e entrega eventos para diferentes destinos, como funções AWS Lambda, filas SQS e mais.

Utiliza uma arquitetura baseada em eventos, onde sistemas ou serviços interagem através de eventos. Um evento é uma mudança de estado ou uma atualização em um sistema, capturada e compartilhada com outros sistemas interessados. Essa abordagem permite comunicação assíncrona, desacoplada e reativa, substituindo chamadas síncronas ou consultas constantes entre serviços.

---

## Funcionamento

O **EventBridge** atua como intermediário entre produtores e consumidores de eventos.

1. **Produção de Evento**:
   - Fontes como DynamoDB, Lambda ou aplicações externas geram eventos e os enviam ao EventBridge.
2. **Regras de Roteamento**:
   - Regras de filtragem determinam o destino dos eventos com base em seus atributos (ex.: campos JSON).
3. **Destino**:
   - Eventos são entregues a destinos como funções Lambda, filas SQS, logs CloudWatch ou serviços SaaS integrados.
4. **Monitoramento e DLQs**:
   - Eventos não entregues são enviados para Dead Letter Queues (DLQs) ou registrados para depuração.

---

## Aplicabilidade

### Quando usar o EventBridge?

- **Automação de Tarefas**: Disparar ações com base em eventos, como executar backups ou enviar notificações.
- **Integração de Sistemas**: Conectar serviços AWS, aplicativos SaaS e sistemas personalizados.
- **Análise de Dados**: Coletar e processar dados de eventos para análises em tempo real.

---

## Casos de Uso

Exemplo:  
Uma empresa de e-commerce utiliza o **Amazon EventBridge** para automatizar o processamento de pedidos. Quando um cliente finaliza uma compra, um evento é enviado ao EventBridge e roteado para três destinos principais:

1. **Faturamento**: Geração de nota fiscal.  
2. **Estoque**: Atualização das quantidades disponíveis.  
3. **Notificação**: Envio de confirmação ao cliente.

Essa abordagem garante que todos os processos sejam executados automaticamente e de forma integrada, melhorando a eficiência e a experiência do cliente.

---

## Características

- **Regras de Roteamento**: Permite filtrar e transformar eventos antes de enviá-los.  
- **DLQs (Dead Letter Queues)**: Garantia de análise posterior para eventos não entregues.  
- **API Flexível**: Recursos para criar, listar, modificar e excluir regras e barramentos.  
- **Escalabilidade Automática**: Gerencia volumes elevados de eventos sem intervenção manual.

---

## Vantagens

- **Integração Simples**: Comunicação entre serviços AWS e sistemas externos sem pipelines complexos.  
- **Alta Escalabilidade**: Suporte a cargas elevadas de eventos sem degradação do desempenho.  
- **Redução de Acoplamento**: Comunicação assíncrona entre serviços, reduzindo dependências.  
- **Custo por Uso**: Cobrança baseada na quantidade de eventos processados.  
- **Flexibilidade**: Configuração de regras e destinos variados para diferentes necessidades.

---

## Desvantagens e Limitações

- **Custo Variável**: Pode ser significativo em ambientes de alto volume de eventos.  
- **Latência**: Não ideal para aplicações que exigem comunicação em tempo real com baixa latência.  
- **Limitações de Configuração**: Regras de filtragem complexas em cenários avançados.  
- **Dependência da AWS**: Integração com sistemas fora da AWS pode ser desafiadora.

---

## Recursos da API

O **Amazon EventBridge** oferece APIs para gerenciamento completo de barramentos, regras e eventos.

### Principais APIs:

- `PutEvents`: Envia eventos para o barramento.  
- `CreateRule`: Cria uma regra para filtrar e rotear eventos.  
- `DeleteRule`: Exclui regras configuradas.  
- `PutTargets`: Define os destinos para onde os eventos serão enviados.  
- `RemoveTargets`: Remove destinos configurados para uma regra.

---

## Conclusão

O **Amazon EventBridge** é uma ferramenta poderosa para arquiteturas modernas baseadas em eventos. Sua capacidade de integrar serviços AWS, SaaS e fontes personalizadas o torna essencial para sistemas desacoplados e reativos.

Apesar das limitações, suas vantagens em termos de escalabilidade, flexibilidade e simplicidade fazem dele uma escolha robusta para diversos cenários. Ao adotá-lo, é fundamental planejar regras de filtragem e monitoramento para garantir um fluxo eficiente de eventos, maximizando seus benefícios.

---

**Gabriel da Silva Pereira**  
**Cintia Mariana Carvalho de Oliveira**  
**Curso de Sistemas de Informação**  
**Pouso Alegre – MG, 2024**
