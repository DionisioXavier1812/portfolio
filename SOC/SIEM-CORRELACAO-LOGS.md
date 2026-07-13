\# 🛡️ Módulo SIEM – Correlação de Logs e Alertas



Este módulo apresenta regras de correlação, padrões de detecção e alertas automáticos utilizados em um ambiente SOC para identificar incidentes com base em logs Sigma e eventos operacionais.



\---



\# 📡 1. Fontes de Logs Monitoradas



\- Painel de alarme (ETH/GPRS)

\- Sensores IVP

\- Sensores magnéticos

\- Bateria e energia AC

\- Eventos Sigma (falha, restauro, disparo, autoteste)

\- Comunicação redundante

\- Logs de vigilância



\---



\# 🔍 2. Regras de Correlação (SIEM)



\## ✔️ Regra 01 – Perda Total de Comunicação

\*\*Condição:\*\*

\- Falha ETH  

\- GPRS Offline  

\- Autoteste não recebido por > 3 minutos  



\*\*Correlação:\*\*



\*\*Ação Automática:\*\*

\- Gerar alerta crítico  

\- Escalonar para vigilância  

\- Registrar no Log.bank  



\---



\## ✔️ Regra 02 – Disparo Indevido IVP após falha

\*\*Condição:\*\*

\- Falha de comunicação  

\- IVP dispara dentro de 5 minutos após falha  



\*\*Correlação:\*\*



\*\*Ação Automática:\*\*

\- Classificar como evento suspeito  

\- Solicitar verificação presencial  



\---



\## ✔️ Regra 03 – Sabotagem (Painel desligado)

\*\*Condição:\*\*

\- Falha AC  

\- Bateria baixa  

\- Comunicação perdida  

\- Todos em sequência < 2 minutos  



\*\*Correlação:\*\*



\*\*Ação Automática:\*\*

\- Alerta crítico  

\- Acionar vigilância imediatamente  



\---



\## ✔️ Regra 04 – Sensor Inoperante

\*\*Condição:\*\*

\- Zona sem movimento  

\- Autoteste sem resposta  

\- > 10 minutos inoperante  



\*\*Correlação:\*\*



\---



\## ✔️ Regra 05 – Comunicação Instável

\*\*Condição:\*\*

\- ETH alternando online/offline  

\- GPRS alternando online/offline  

\- > 3 oscilações em 10 minutos  



\*\*Correlação:\*\*



\---



\# 🚨 3. Tipos de Alertas SIEM



| Severidade | Descrição | Ação |

|-----------|-----------|------|

| 🔴 Crítico | Sabotagem, perda total de comunicação | Ação imediata |

| 🟠 Alto | Falha de energia, falha de bateria | Monitoramento + vigilância |

| 🟡 Médio | Comunicação instável, sensor inoperante | Acompanhamento |

| 🟢 Baixo | Restauros, eventos normais | Registro |



\---



\# 🧠 4. Fluxo de Investigação SIEM





\---



\# 📈 5. Dashboard de Alertas (ASCII)





\---



\# 🎯 Conclusão



Este módulo SIEM demonstra:

\- capacidade de criar regras de correlação  

\- entendimento de padrões operacionais  

\- análise avançada de logs  

\- resposta automatizada a incidentes  

\- visão profissional de SOC  



\---



\# 👤 Autor



\*\*Dionisio Aparecido da Silva Xavier\*\*  

Analista SOC • SIEM • Monitoramento • Resposta a Incidentes



