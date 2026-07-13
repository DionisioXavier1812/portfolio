\# Incidente Simulado – Falha de Comunicação + Disparos Indevidos



\## Cenário

Durante o plantão, o Sistema Sigma reportou:

\- Falha de via ETH

\- GPRS Offline

\- Autoteste não recebido (Partição 000)

\- Disparos indevidos na Partição 001 – Zona 03 (IVP)



\## Linha do Tempo

\- 22:14 – Recebido evento: Falha ETH

\- 22:15 – Recebido evento: GPRS Offline

\- 22:16 – Recebido evento: Autoteste não recebido

\- 22:18 – Disparo indevido IVP (Zona 03)

\- 22:19 – Evento encaminhado para “Em espera”

\- 22:20 – Contato com vigilância operacional

\- 22:22 – Evento encaminhado para “Deslocamento”

\- 22:41 – Vigilante no local → evento marcado como “No local”

\- 22:55 – Restauro parcial da comunicação

\- 23:10 – Restauro total → evento encerrado



\## Análise Técnica

\- Falha simultânea ETH + GPRS indica perda total de comunicação.

\- Autoteste não recebido confirma ausência de sinal.

\- Disparos indevidos sugerem sensor instável ou interferência.



\## Ação

Abertura de chamado no Log.bank:



\*\*Modelo utilizado:\*\*

Partição 001 – Zona 03, DISPARO INDEVIDO IVP.

(FALHA DE VIA ETH / GPRS / AUTOTESTE NÃO RECEBIDO)

MARCA / MODELO: BOSCH

Solicitamos manutenção de SISTEMA ALARME conforme dados acima.



\## Resultado

\- Comunicação restabelecida

\- Sensor IVP revisado

\- Unidade normalizada



