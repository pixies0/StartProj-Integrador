# Considerações

```
1. DEFINIR A TELA PRINCIPAL (PONTO DE ENTRADA)
Hoje vocês têm uma página inicial com texto explicativo.

Mas isso não resolve o problema do usuário.

Tela principal = onde o usuário vê suas finanças

Sugestão:

Saldo atual (principal destaque)
Lista de transações recentes
Botão: “Adicionar despesa”
```
```
2. DEFINIR O FLUXO DO USUÁRIO (ESSENCIAL)
Usuário entra → vê saldo → adiciona despesa → sistema atualiza → visualiza extrato

Atualmente:
não existe fluxo funcional
só navegação visual (navbar)
```
```
3. SEPARAR FUNCIONALIDADES POR ETAPA
Etapa 1 — Visualizar saldo
De onde vem esse valor?

Etapa 2 — Criar despesa
Quais dados serão inseridos?

Etapa 3 — Salvar despesa
Onde isso será armazenado?

Etapa 4 — Atualizar extrato
Como os dados aparecem na tela?

Atualmente nenhuma dessas etapas existe de fato
```
```
4. DEFINIR PARA ONDE AS AÇÕES VÃO
Navbar tem opções:
Home / Extrato / Criar Despesa

Mas:

Clicar nelas não faz nada ainda

Toda ação precisa gerar consequência

Exemplo:

Criar despesa → abre formulário
Salvar → adiciona na lista
Extrato → mostra dados
```
```
5. O QUE O SISTEMA PRECISA “LEMBRAR”

{
  "tipo": "despesa",
  "descricao": "Lanche",
  "valor": 25,
  "data": "2026-05-06"
}
```

# SUGESTÃO FUNCIONALIDADES
```
1. Criar formulário de despesa (PRIORIDADE)
Campos:
- descrição
- valor
- tipo (entrada/saída)

2. Salvar no localStorage
Ao clicar em salvar → guardar dados

3. Exibir lista de transações
Mostrar na tela

4. Calcular saldo automático
Somar entradas - despesas

5. Atualizar interface dinamicamente
Sem recarregar página

6. Botão de exclusão
Remover item

7. Feedback visual
Mensagem de sucesso

8. Integração com API
ExchangeRate API:
→ converter saldo para outra moeda
```

## Ponto Positivo
Uso de Bootstrap (boa decisão)

Estrutura inicial de navegação pronta

## Ponto Crítico
Sistema ainda não começou

- não há JS funcional
- não há dados
- não há interação

Interface não representa funcionalidade
- só texto e navbar
- nenhuma ação real