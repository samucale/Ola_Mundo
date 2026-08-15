# Projeto Automação — Departamento de Compras CIP

Repositório central do projeto de automação das tarefas administrativas do
departamento de compras da CIP (Congregação Israelita Paulista).

> **Objetivo:** automatizar as tarefas que eram feitas manualmente pela
> assistente administrativa — lançamento de notas fiscais, compras online,
> compras com fornecedores rotineiros e contas a pagar — usando Make.com,
> Zoho Books e IAs (Claude / ChatGPT) trabalhando em conjunto.

---

## Como usar este repositório

Cada área do projeto tem sua própria pasta, com um arquivo `README.md`
que traz o **estado atual** no topo. Antes de mexer em qualquer coisa,
abra a pasta da área e leia o status.

**Legenda de status:**
- ✅ Funcionando — em produção, rodando bem
- 🟡 Em ajuste — funciona parcialmente ou precisa de conserto
- 🔴 Com problema — quebrado ou inválido
- ⚪ A fazer — ainda não iniciado

---

## Mapa das áreas

| Área | Pasta | Estado |
|------|-------|--------|
| Compras online | [`/compras-online`](./compras-online) | ✅ Funcionando |
| Notas fiscais (NF-e → Zoho) | [`/notas-fiscais`](./notas-fiscais) | 🟡 Em ajuste |
| Contas a pagar | [`/contas-a-pagar`](./contas-a-pagar) | ⚪ A fazer |
| Infraestrutura (Make, Zoho, IAs, servidor) | [`/infraestrutura`](./infraestrutura) | 🟡 Em ajuste |

---

## Ferramentas do projeto — quem faz o quê

| Ferramenta | Papel |
|------------|-------|
| **Make.com** | Motor das automações (executa os fluxos de verdade) |
| **Zoho Books** | Sistema financeiro da CIP (despesas, cobranças/bills, pagamentos) |
| **Google (Forms, Sheets, Drive, Email)** | Entrada de dados, planilhas de controle, arquivos, avisos |
| **Asana** | Gestão de tarefas do fluxo de compras |
| **Claude / ChatGPT** | Planejar fluxos, revisar lógica, processar texto/imagem, documentar |
| **GitHub (este repo)** | Documentação central e histórico do projeto |

---

## Regras de trabalho (para evitar confusão)

Como várias IAs e o próprio Sami podem mexer no projeto, seguimos regras
simples para não gerar ruído:

1. **Status sempre visível.** Todo arquivo de área começa com o estado atual.
2. **Cada tarefa numa branch separada.** Nunca duas IAs mexendo no mesmo
   trecho ao mesmo tempo. Só depois de revisado, junta na `main`.
3. **Commits frequentes e pequenos.** Salvar o progresso sempre, para que
   outra IA (ou outra conta) possa continuar de onde parou.
4. **Uma fonte de verdade.** A documentação vive aqui no GitHub. O que está
   fora daqui (cenário no Make, planilha no Sheets) é apontado por link, não
   copiado.

---

## Estado geral do projeto (atualizado manualmente)

- Compras online: rodando em produção há semanas, saudável.
- Notas fiscais: várias tentativas feitas; o cenário "Unificado" no Make é a
  aposta atual, mas ainda não foi testado/ativado.
- Contas a pagar: definido que serão lançadas como **Cobranças (Bills)** no
  Zoho. Ainda a desenhar.
- Infraestrutura: Make já em uso; decisões sobre servidor e uso conjunto das
  IAs ainda em aberto.
