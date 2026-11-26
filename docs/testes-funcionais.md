
# Relatório de Testes Funcionais - TechFix OS

## 1. Identificação

- Projeto: TechFix OS
- Grupo: 3
- Responsável pelos testes: HildegardeMelo
- Data: 26/11/2026
- Sprint: Sprint Final | Validação e Entrega A3
- Ambiente: Aplicação web publicada na Vercel
- Navegador: Microsoft Edge
- Ordem de serviço utilizada: OS #1042

## 2. Objetivo

Verificar o comportamento das funcionalidades do sistema, identificar falhas e registrar evidências para análise e correção antes da entrega final do projeto.

## 3. Metodologia

Foram realizados testes manuais na interface do sistema, simulando a jornada de atendimento de uma assistência técnica, desde a recepção do equipamento até a visualização da garantia.

## 4. Resultados dos testes

| ID | Funcionalidade | Resultado |
|---|---|---|
| TF01 | Visualização da triagem | Aprovado visualmente |
| TF02 | Validação de campos obrigatórios | Aprovado no cenário observado |
| TF03 | Criação da ordem de serviço | Aprovado na interface |
| TF04 | Seleção de condições do equipamento | Aprovado na interface |
| TF05 | Inclusão de bateria no orçamento | Aprovado |
| TF06 | Aplicação de desconto PIX | Aprovado |
| TF07 | Aprovação do orçamento | Aprovado na interface |
| TF08 | Atualização do status do reparo | Falha em investigação |
| TF09 | Atualização dos valores no checkout | Aprovado |
| TF10 | Inclusão de acessórios | Aprovado |
| TF11 | Exportação da nota fiscal em PDF | Reprovado |
| TF12 | Visualização da garantia de 90 dias | Aprovado visualmente |

## 5. Validação dos cálculos

Durante os testes de orçamento e checkout, foram observados os seguintes valores:

- Orçamento inicial: R$ 630,00
- Inclusão de bateria: R$ 150,00
- Novo subtotal: R$ 780,00
- Desconto PIX de 10%: R$ 78,00
- Total com desconto: R$ 702,00
- Inclusão de película: R$ 35,00
- Total final: R$ 737,00

Resultado: os cálculos apresentados na interface corresponderam aos valores esperados.

## 6. Falhas identificadas

### BUG 01 - Exportação incompleta da nota fiscal

Issue: #33

Resultado esperado:
O PDF deve apresentar todas as informações exibidas no checkout.

Resultado obtido:
O documento exportado apresentou apenas o cabeçalho e os dados do cliente, com o restante do conteúdo cortado.

Prioridade sugerida: Alta.

Status: Aguardando correção.

### BUG 02 - Atualização das etapas do reparo

Issue: #34

Resultado esperado:
O responsável autorizado deve conseguir atualizar as etapas do reparo.

Resultado obtido:
Não foi possível avançar de "Em Reparo" para "Testes" pela interface apresentada.

Prioridade sugerida: Alta.

Status: Aguardando investigação e correção, caso confirmada a falha.

## 7. Garantia

A interface apresentou corretamente:

- Identificação da OS #1042.
- Indicador de garantia ativa.
- Prazo de 90 dias.
- Barra de progresso.
- Informação de retirada.
- Previsão de arquivamento no 91º dia.

A contagem automática dos dias e o arquivamento ainda precisam ser validados.

## 8. Evidências

As evidências foram coletadas por meio de capturas de tela e do arquivo PDF gerado durante os testes.

Os registros das falhas estão disponíveis nas Issues #33 e #34.

## 9. Testes pendentes

- Recusa de orçamento.
- Cancelamento de serviço com justificativa obrigatória.
- Persistência dos dados.
- Controle de permissões.
- Contagem automática da garantia.
- Arquivamento automático.
- Retestes após a correção das falhas.
- Validação da integração com serviços externos.

## 10. Conclusão

Os testes demonstraram que parte do fluxo de atendimento funciona conforme o esperado na interface apresentada.

Foram identificadas duas ocorrências que precisam de análise técnica antes da validação definitiva do sistema.

O registro dessas ocorrências contribui para a melhoria da qualidade, rastreabilidade dos requisitos e confiabilidade da aplicação.

A aprovação definitiva depende da correção das falhas e da execução dos testes pendentes.

## 11. Referências

- Issue #18 - Casos de uso.
- Pull Request #32 - Documentação dos casos de uso.
- Issue #33 - Exportação incompleta do PDF.
- Issue #34 - Atualização do status do reparo.
- Documento docs/casos-de-uso.md.
