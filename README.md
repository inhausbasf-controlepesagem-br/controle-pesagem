# Controle de Pesagem (BASF) — Automação, Rastreabilidade e Exportação Padronizada

Aplicação web para controle diário de pesagem de bags envasados, substituindo registros em papel por um fluxo digital com rastreabilidade, governança de acesso e exportação no padrão operacional da logística.

## 🔗 Links
- **Demo (GitHub Pages):** https://inhausbasf-controlepesagem-br.github.io/controle-pesagem/
- **Repositório:** https://github.com/inhausbasf-controlepesagem-br/controle-pesagem

## 🎯 Objetivo
Automatizar o processo de pesagem, eliminando papel e elevando:
- confiabilidade dos registros
- rastreabilidade/auditoria
- padronização na exportação para logística

## 🧩 Funcionalidades
### Cadastro de pesagem (campos)
- Data
- Lote
- Turno
- Operadores do turno
- Pesado por
- Modelo de embalagem
- Peso programado (kg)
- BAG nº
- Peso bruto (kg)
- Peso líquido (kg)

### Perfis e permissões (RBAC)
- **Supervisor**
  - Acesso total: cadastro, exclusão e exportação
- **Operador**
  - Cadastro e exportação (uso principal: cadastro)
  - **Janela de 15 minutos para exclusão** em caso de lançamento incorreto
  - Após 15 minutos, apenas Supervisor pode excluir
- **Exportador**
  - Apenas exportação
  - Exporta dados filtrando por **data, lote e modelo de embalagem**
  - Gera arquivo Excel no **formato utilizado pela logística**, com fórmulas agregadas

## 📈 Resultado
Projeto adotado e utilizado como procedimento na planta, substituindo o processo manual em papel e aumentando rastreabilidade do fluxo.

## 🔐 Segurança (visão geral)
Controle de permissões por perfil (RBAC) e restrições específicas por ação (ex.: regra de tempo para exclusão por Operador).

## 🗺️ Roadmap (próximos passos)
- [ ] Auditoria/logs avançados (quem alterou/excluiu e quando)
- [ ] Dashboard de indicadores (por lote/turno/modelo)
- [ ] CI/CD (lint/test/deploy) no GitHub Actions
- [ ] Sanitização total para versão demo (sem dados reais)

## ⚠️ Observação
A demo deve utilizar dados fictícios, sem qualquer informação sensível/operacional.
