# Considerações

1. DEFINIR A TELA PRINCIPAL (PONTO DE ENTRADA)

```
Formulário direto, mas isso não está claro como “início”.

Tela principal = onde o usuário começa a experiência

Tela principal sugerida: (Template Bootstrap)

Nome da barbearia
Botão: “Agendar horário”
Lista de horários do dia
```

2. DEFINIR O FLUXO DO USUÁRIO (ESSENCIAL)(EXERCÍCIO MENTAL)
```
Usuário entra → escolhe serviço → escolhe data → vê horários → seleciona → confirma → recebe feedback
```

3. SEPARAR FUNCIONALIDADES POR ETAPA (PENSAMENTO ESTRUTURADO DO SISTEMA)

```
Cada parte do sistema resolve uma coisa específica

Etapa 1 — Escolha de serviço
O que acontece?
O que o sistema precisa guardar?
Etapa 2 — Escolha de data
Filtra horários?
Existe validação?
Etapa 3 — Horários disponíveis
Quem gera?
São fixos ou dinâmicos?
Etapa 4 — Confirmação
O que é exibido?
O que é salvo?
```

4. DEFINIR PARA ONDE AS AÇÕES VÃO
```
Evitar botões sem destino claro.

Toda ação precisa gerar uma consequência

Exemplos:

Clicar em “Ver horários” → carrega horários
Clicar em horário → seleciona
Clicar em confirmar → salva + mostra mensagem

Isso é fluxo informacional
```

5. O QUE O SISTEMA PRECISA “LEMBRAR”

```
Pensem no estado da informação

{
  barbeiro: "João",
  servico: "Corte",
  data: "2026-05-10",
  horario: "14:00"
}
```

# SUGESTÃO FUNCIONALIDADES

```
1. Agendamento por horário
Fluxo principal: Captura a data atual e escolhe horário
Fluxo alternativo: Jogar agendamento no horário para o próximo dia

2. Confirmação de agendamento
Botão “Confirmar”
Exibir resumo do agendamento

Exemplo:

Barbeiro: João
Serviço: Corte
Data: 10/05
Hora: 14:00

3. Persistência com localStorage
Salvar agendamento
Manter dados ao recarregar página

👉 Simula backend

4. Listagem de agendamentos
Mostrar agendamentos feitos
Exibir em lista ou cards

5. Feedback visual
Toast / alerta de sucesso

Mensagem tipo:

“Agendamento realizado com sucesso”

6. Estados visuais dos horários
Verde → disponível
Vermelho → ocupado
Cinza → desabilitado

7. Cancelamento de agendamento
Botão “Cancelar”
Remove do localStorage

8. Edição de agendamento
Alterar horário ou data
```

---

⚙️ FUNCIONALIDADES INTERMEDIÁRIAS (PRÓXIMO NÍVEL)
1. Bloqueio de horários já ocupados
Horário agendado → fica desabilitado

👉 Introduz regra de negócio

6. Múltiplos barbeiros
Select dinâmico
Cada barbeiro pode ter horários diferentes

👉 Mais realista

7. Serviços dinâmicos
Tempo diferente por serviço
(ex: corte = 30min, barba = 20min)

👉 Abre espaço para lógica futura

8. Filtro por data
Mostrar horários apenas após escolher data

👉 Fluxo mais profissional

🌐 FUNCIONALIDADES COM API (OBRIGATÓRIO EVOLUIR)
9. Cliente automático (API)
Random User API
Aplicação:
Ao confirmar agendamento → associar cliente
Exibir nome do cliente
10. Datas indisponíveis
Nager.Date API
Aplicação:
Bloquear datas no calendário
🎨 FUNCIONALIDADES DE INTERFACE (DIFERENCIAL)
11. Feedback visual
Toast / alerta de sucesso

Mensagem tipo:

“Agendamento realizado com sucesso”

12. Estados visuais dos horários
Verde → disponível
Vermelho → ocupado
Cinza → desabilitado
13. Loader (carregamento)
Ao buscar horários ou API
Exibir “Carregando...”

👉 Simula sistema real

🧠 FUNCIONALIDADES MAIS AVANÇADAS (SE SOBRAR TEMPO)
14. Cancelamento de agendamento
Botão “Cancelar”
Remove do localStorage
15. Edição de agendamento
Alterar horário ou data
16. Simulação de lembrete

Mostrar mensagem:

“Você tem um agendamento em breve”

(Não precisa notificação real)
