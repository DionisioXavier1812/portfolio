\# 🧠 Mapa Mental Completo – SOC + SIEM + PIR



Este mapa mental consolida todo o fluxo operacional do SOC, incluindo monitoramento, correlação SIEM, resposta a incidentes e análise pós-incidente (PIR).  

Formato visual, técnico e profissional.



====================================================================

&#x20;                       🛡️ SOC – VISÃO GERAL

====================================================================



&#x20;                       \[MONITORAMENTO]

&#x20;                             |

&#x20;                             v

&#x20;                   \[DETECÇÃO DE EVENTOS]

&#x20;                             |

&#x20;                             v

&#x20;                   \[CLASSIFICAÇÃO INICIAL]

&#x20;                (Intrusão, Falha, Sabotagem,

&#x20;             Comunicação, Energia, Bateria, IVP)

&#x20;                             |

&#x20;                             v

&#x20;                       \[AÇÃO SOC]

&#x20;                - Registro Log.bank

&#x20;                - Acionamento vigilância

&#x20;                - Testes remotos

&#x20;                - Verificação de sensores

&#x20;                             |

&#x20;                             v

&#x20;                       \[ESCALONAMENTO]

&#x20;                - Técnico

&#x20;                - Supervisor

&#x20;                - Segurança Física

&#x20;                - Engenharia

&#x20;                             |

&#x20;                             v

&#x20;                       \[ENCERRAMENTO]

&#x20;                - Normalizado

&#x20;                - Restauro

&#x20;                - Substituição

&#x20;                - Manutenção

&#x20;                             |

&#x20;                             v

&#x20;                       \[GERAÇÃO PIR]



====================================================================

&#x20;                       📡 CAMADAS DE COMUNICAÇÃO

====================================================================



ETH (Rede Cabeada)

&#x20;   └── Falha ETH → Risco de perda parcial

GPRS (Rede Celular)

&#x20;   └── Oscilação → Redundância instável

Autoteste

&#x20;   └── Ausente → Falha de sensor ou comunicação

Painel

&#x20;   └── AC / Bateria / Comunicação / Sensores



Fluxo:

ETH → GPRS → Autoteste → Painel → SOC



====================================================================

&#x20;                       🎯 INCIDENTES SOC

====================================================================



\[Intrusão] ------------> Sensor magnético OK

\[IVP Falha] -----------> Zona inoperante

\[Sabotagem] -----------> Painel desligado manualmente

\[Perda de Energia] ----> Falha AC prolongada

\[Falha de Bateria] ----> < 11.5V

\[Porta Violada] -------> Abertura indevida

\[Sensor Inoperante] ---> Sem movimento

\[Comunicação Instável] -> ETH/GPRS oscilando



====================================================================

&#x20;                       🔍 SIEM – CORRELAÇÃO

====================================================================



Regra 01 – Perda Total de Comunicação

IF ETH\_FAIL AND GPRS\_OFFLINE AND AUTOTESTE\_AUSENTE

→ ALERTA CRÍTICO



Regra 02 – Disparo Indevido IVP

IF COMMS\_FAIL AND IVP\_DISPARO <= 5min

→ ALERTA ALTO



Regra 03 – Sabotagem

IF AC\_FAIL AND BAT\_LOW AND COMMS\_LOST <= 2min

→ ALERTA CRÍTICO



Regra 04 – Sensor Inoperante

IF ZONA\_INOPERANTE AND AUTOTESTE\_AUSENTE >= 10min

→ ALERTA MÉDIO



Regra 05 – Comunicação Instável

IF OSC\_ETH >= 3 AND OSC\_GPRS >= 3

→ ALERTA MÉDIO



====================================================================

&#x20;                       🚨 TIPOS DE ALERTA

====================================================================



🔴 Crítico → Sabotagem, perda total de comunicação  

🟠 Alto → Falha AC, bateria baixa  

🟡 Médio → Comunicação instável, sensor inoperante  

🟢 Baixo → Restauros, eventos normais  



====================================================================

&#x20;                       📈 DASHBOARD DE ALERTAS

====================================================================



CRÍTICOS:      ████░░ 40%

ALTOS:         ███░░░ 30%

MÉDIOS:        ██░░░░ 20%

BAIXOS:        █░░░░░ 10%



====================================================================

&#x20;                       🧪 LOGS SIGMA (RESUMO)

====================================================================



22:14 Falha ETH  

22:15 GPRS Offline  

22:16 Autoteste ausente  

22:18 Disparo IVP  

22:20 Evento em deslocamento  

22:41 Vigilante no local  

22:55 Restauro parcial  

23:10 Restauro total  



====================================================================

&#x20;                       🧭 FLUXO COMPLETO SOC + SIEM + PIR

====================================================================



\[Monitoramento]  

&#x20;     ↓  

\[Detecção]  

&#x20;     ↓  

\[Correlação SIEM]  

&#x20;     ↓  

\[Classificação SOC]  

&#x20;     ↓  

\[Ação Operacional]  

&#x20;     ↓  

\[Escalonamento]  

&#x20;     ↓  

\[Normalização]  

&#x20;     ↓  

\[Coleta de Evidências]  

&#x20;     ↓  

\[PIR – Post Incident Review]  

&#x20;     ↓  

\[Melhoria Contínua]



====================================================================

&#x20;                       👤 Autor

====================================================================



\*\*Dionisio Aparecido da Silva Xavier\*\*  

Analista SOC • SIEM • Monitoramento • Resposta a Incidentes



