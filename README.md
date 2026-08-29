# Índice · FINANCIAMIENTO.md

- [1. Requisitos de Stellar Community Fund](#1-requisitos-de-stellar-community-fund)
- [2. Funcionamiento de Drips Protocol](#2-funcionamiento-de-drips-protocol)
- [3. Backlog por fases ligado al financiamiento](#3-backlog-por-fases-ligado-al-financiamiento)
- [4. El hueco honesto](#4-el-hueco-honesto)
- [5. Uso de fuentes primarias, incluidas en inglés](#5-uso-de-fuentes-primarias-incluidas-en-inglés)

---

# REPOSITORIO E INFRAESTRUCTURA FINANCIERA (STELLAR / DRIPS)

## 1. Requisitos de Stellar Community Fund

El **Stellar Community Fund (SCF)** es el programa oficial de becas de la Stellar Development Foundation (SDF) para financiar proyectos construidos sobre Stellar y Soroban. En enero de 2026 se lanzó **SCF 7.0**, la versión vigente al momento de esta consulta.

**Cómo se postula:**
1. Se llena el *Interest Form* en el sitio oficial.
2. Un panel evalúa el valor potencial del proyecto para el ecosistema Stellar/Soroban.
3. Si se aprueba la elegibilidad, el equipo es invitado a enviar una propuesta completa a una de tres modalidades del **SCF Build Award**: Open, Integration o RFP.
4. La propuesta pasa por *prescreen*, revisión de panel y, en la modalidad Open, voto de la comunidad.

**Montos y forma de pago:** hasta **150,000 USD en XLM**, pagados en 4 tramos ligados a hitos, pensados para cubrir hasta 4-6 meses de desarrollo hasta el lanzamiento en Mainnet. El valor se cotiza en USD pero se paga en XLM según el índice XLM-USD de CF Benchmarks.

**Requisitos de elegibilidad clave:**
- Stellar/Soroban debe tener un rol central y genuino en el proyecto, no forzado.
- Individuos, equipos y entidades pueden postular.
- No aplica si el proyecto ya recibe fondos activos de programas con objetivos traslapados (Matching Fund, Enterprise Fund, becas de investigación con entregables pendientes).
- SDF puede exigir verificación KYC/KYB en cualquier momento.
- Al aprobarse, se obtiene acceso al Stellar LaunchKit (créditos de auditoría, infraestructura, conexión con aceleradoras).

> **Fuente:** Stellar Development Foundation, *SCF Handbook — Build Award*, https://stellar.gitbook.io/scf-handbook/scf-awards/build-award — consultado 26/08/2026.

[⬆ volver al índice](#índice--financiamientomd)

---

## 2. Funcionamiento de Drips Protocol

**Drips** es un protocolo de contratos inteligentes desplegado sobre Ethereum y redes compatibles con EVM (Ethereum mainnet, Optimism, Metis y Filecoin), pensado para financiar de forma continua proyectos de código abierto. No pertenece a Stellar Development Foundation; se integra con GitHub.

**Cómo funciona el streaming:**
- Cualquiera puede crear una **Drip List**: hasta 200 repositorios de GitHub, direcciones Ethereum u otras Drip Lists, cada una con un porcentaje asignado.
- Los fondos se transmiten como un **flujo continuo por segundo** de cualquier token ERC-20, modificable o detenible en cualquier momento.
- El flujo se **liquida periódicamente** (mensual en Ethereum mainnet, diario en otras redes) y se reparte automáticamente, propagándose hacia las dependencias declaradas.

**Qué se necesita para recibir fondos:**
1. Un repositorio de código abierto en GitHub (o uno vacío, si solo se quiere representar a la organización).
2. Publicar un archivo `FUNDING.json` en la rama por defecto, con la dirección Ethereum a verificar on-chain.
3. Una billetera Ethereum con algo de ETH para el gas del reclamo (en redes como Filecoin, Drips puede cubrirlo).
4. Configurar el porcentaje repartido entre mantenedores y dependencias.

**Límites importantes:** máximo 200 destinatarios por Drip List. El streaming **no opera de forma nativa en Stellar/Soroban** — corre en Ethereum/EVM. La única integración confirmada con Stellar es **Drips Wave**: ciclos semanales de recompensas por resolver issues de GitHub, financiados por SDF y liquidados en Stellar, distinto del streaming continuo.

> **Fuente:** Drips Network, *Introduction* y *Claim your open-source project*, https://docs.drips.network/ — consultado 26/08/2026.

[⬆ volver al índice](#índice--financiamientomd)

---

## 3. Backlog por fases ligado al financiamiento

Ejemplo de estructura para relacionar el backlog con las fuentes de financiamiento investigadas. Sustituyan los corchetes con las fases reales de su proyecto:

| Fase | Objetivo del backlog | Financiamiento | Justificación |
|---|---|---|---|
| Fase 1: Fundación | [MVP funcional en testnet] | SCF Build — Track Open, 1er tramo | El primer tramo está pensado para llevar un proyecto validado a un MVP demostrable. |
| Fase 2: Comunidad | [Abrir issues a colaboradores] | Drips Wave (Stellar) | Wave paga por resolver issues puntuales y liquida en Stellar, sin requerir un Drip List propio. |
| Fase 3: Mainnet | [Despliegue en Stellar Mainnet] | SCF Build, tramos 3–4 | Los tramos finales se liberan al validar hitos de lanzamiento, el criterio que evalúa el panel. |
| Fase 4: Sostenibilidad | [Financiamiento continuo de mantenimiento] | Drip List (Ethereum/EVM) | Streaming continuo de dependencias una vez reclamado el repo — canal adicional, no en Stellar. |

[⬆ volver al índice](#índice--financiamientomd)

---

## 4. El hueco honesto

Al 28 de agosto de 2026, la investigación muestra un hueco real: el equipo **no ha verificado si el streaming continuo de Drips (Drip Lists) es compatible de forma nativa con Stellar/Soroban**. Lo confirmado es que ese streaming corre sobre Ethereum/EVM, y que la única integración de Drips con Stellar hoy es Drips Wave, que paga tareas de GitHub, no financiamiento continuo por dependencias.

**Plan para cerrarlo:** contactar al equipo de Drips (Discord o docs.drips.network) para confirmar si existe o está planeada una ruta de streaming compatible con Soroban, o si por ahora la única opción realista es combinar Drips Wave (recompensas puntuales) con una tesorería paralela en Ethereum/EVM para el streaming continuo.

> **Fecha estimada de cierre:** [definir con el equipo].

[⬆ volver al índice](#índice--financiamientomd)

---

## 5. Uso de fuentes primarias, incluidas en inglés

1. Stellar Development Foundation, *SCF Handbook — Build Award* — https://stellar.gitbook.io/scf-handbook/scf-awards/build-award (inglés)
2. Stellar Development Foundation, *SCF Handbook — Submission Criteria* — https://stellar.gitbook.io/scf-handbook/scf-awards/build-award/submission-criteria (inglés)
3. Drips Network, *Introduction* — https://docs.drips.network/ (inglés)
4. Drips Network, *Claim your open-source project* — https://docs.drips.network/get-support/claim-your-repository/ (inglés)
5. Drips Network, *Participating in a Wave* — https://docs.drips.network/wave/maintainers/participating-in-a-wave/ (inglés)

[⬆ volver al índice](#índice--financiamientomd)
