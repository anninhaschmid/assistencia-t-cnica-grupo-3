# Casos de Uso e Requisitos Não Funcionais

## Projeto TechFlix OS

Responsável: Hildegarde Nascimento de Melo
Atividade relacionada: Issue #18
Sprint Final: Validação e Entrega A3

## 1. Objetivo

Documentar o comportamento esperado do sistema de assistência técnica, estabelecendo regras de negócio e critérios de aceitação.

## 2. Caso de Uso UC01: Aprovação de Orçamento

**Ator principal:** Cliente.

**Pré-condição:** Ordem de serviço cadastrada e orçamento disponível.

### Fluxo principal

1. O cliente consulta a ordem de serviço.
2. O sistema apresenta os valores de peças e mão de obra.
3. O cliente consulta as condições e os prazos.
4. O cliente aprova o orçamento e aceita o termo.
5. O sistema registra a decisão.
6. A equipe técnica recebe a autorização para iniciar o reparo.

### Fluxo alternativo

Caso o cliente não aprove o orçamento, o reparo não deverá ser iniciado.

### Critério de aceitação

O sistema deverá registrar a decisão do cliente, a data e as condições do orçamento aprovado.

## 3. Caso de Uso UC02: Atualização do Reparo

**Ator principal:** Técnico.

**Pré-condição:** Ordem de serviço ativa.

### Fluxo principal

1. O técnico acessa a ordem de serviço.
2. Seleciona a etapa atual do reparo.
3. Registra as atividades realizadas.
4. Adiciona evidências por fotos ou vídeos.
5. Confirma a atualização.
6. O sistema disponibiliza o progresso para acompanhamento do cliente.

### Critério de aceitação

As atualizações deverão permanecer associadas à ordem de serviço e ao técnico responsável.

## 4. Caso de Uso UC03: Cancelamento de Serviço

**Atores:** Técnico e recepção.

### Cenário de consenso

O técnico precisa ter autonomia para solicitar o cancelamento de um serviço, enquanto a recepção necessita de uma justificativa registrada.

### Solução proposta

Permitir o cancelamento mediante preenchimento obrigatório do motivo.

### Fluxo principal

1. O técnico acessa a ordem de serviço.
2. Seleciona a opção de cancelamento.
3. Informa o motivo.
4. Confirma a operação.
5. O sistema registra o cancelamento.
6. A recepção consulta a justificativa registrada.

### Regra de negócio

RN01: Não permitir o cancelamento sem justificativa.

RN02: Preservar o histórico da ordem de serviço.

RN03: Registrar o responsável e a data do cancelamento.

### Critério de aceitação

Uma tentativa de cancelamento sem justificativa deverá ser bloqueada pelo sistema.

## 5. Requisitos Não Funcionais

### RNF01: Segurança

Restringir operações administrativas aos usuários autorizados.

### RNF02: Rastreabilidade

Registrar o responsável, a data e as alterações relevantes realizadas nas ordens de serviço.

### RNF03: Integridade dos Dados

Preservar os registros anteriores durante atualizações e cancelamentos.

### RNF04: Usabilidade

Apresentar mensagens claras de confirmação, erro e preenchimento obrigatório.

### RNF05: Privacidade

Restringir o acesso aos dados pessoais e às evidências dos clientes.

## 6. Cenários de Teste

| ID | Cenário | Resultado esperado |
|---|---|---|
| CT01 | Aprovar orçamento | Registrar o aceite |
| CT02 | Recusar orçamento | Não autorizar o reparo |
| CT03 | Atualizar etapa | Registrar novo status |
| CT04 | Anexar evidência | Associar arquivo à OS |
| CT05 | Cancelar sem motivo | Bloquear operação |
| CT06 | Cancelar com motivo | Registrar cancelamento |
| CT07 | Acesso não autorizado | Bloquear acesso |

## 7. Situação da Validação

Os casos de uso e critérios de aceitação estão documentados.

A implementação e a execução dos testes deverão ser verificadas no sistema antes da classificação definitiva dos requisitos.

## 8. Referências

- Issue #18
- README.md
- ARCHITECTURE.md
- Documentação da concepção e dos requisitos do TechFlix OS
