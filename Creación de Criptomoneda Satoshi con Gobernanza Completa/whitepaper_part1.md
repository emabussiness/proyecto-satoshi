# Whitepaper: SatoshiWasHere ($SWH)

**Versión 1.0 - Mayo 2025**

**ADVERTENCIA:** Este documento es conceptual y describe un proyecto experimental. La inversión en criptomonedas conlleva un alto riesgo. Realice su propia investigación (DYOR).

## 1. Introducción: El Eco de un Fantasma Digital

En los anales de la era digital, una figura permanece envuelta en el misterio: Satoshi Nakamoto, el creador seudónimo de Bitcoin. Su identidad, sus motivaciones y su paradero final son objeto de especulación y leyenda. SatoshiWasHere ($SWH) nace como un homenaje a este enigma, un token ERC-20 que busca capturar la esencia de lo desconocido, lo críptico y el potencial disruptivo que Satoshi desató en el mundo.

No pretendemos ser Satoshi, ni resolver el misterio. Somos un eco, una firma dejada en la blockchain, un recordatorio de que las ideas más poderosas a menudo provienen de las sombras. $SWH es un experimento social y tecnológico, una invitación a explorar la intersección entre la criptografía, el arte digital y la narrativa colectiva.

## 2. Filosofía: El Misterio como Protocolo

El núcleo de SatoshiWasHere se basa en varios principios:

*   **Anonimato y Misterio:** Inspirados en Satoshi, abrazamos lo desconocido. La estética, la comunicación y el desarrollo del ecosistema reflejarán este tema central.
*   **Deflación Programada:** Al igual que la escasez inherente de Bitcoin, $SWH incorpora mecanismos deflacionarios. Un impuesto del 2% en cada transferencia es quemado irrevocablemente, reduciendo el suministro total con cada transacción y recompensando a los holders a largo plazo.
*   **Gobernanza Centralizada (Inicial):** Para garantizar la visión inicial y la agilidad en las primeras fases, el contrato es `Ownable`, permitiendo al creador gestionar parámetros clave como el impuesto de transferencia y la funcionalidad de pausa. La descentralización futura es una posibilidad a explorar por la comunidad.
*   **Comunidad y Participación:** Aunque el origen es misterioso, el futuro se construye colectivamente. Buscamos fomentar una comunidad de exploradores, criptógrafos aficionados y entusiastas del enigma de Satoshi.

## 3. El Token $SWH: Especificaciones Técnicas

$SWH es un token estándar ERC-20 desplegado en una blockchain compatible con EVM (Ethereum Virtual Machine), como Ethereum, BNB Chain o Polygon (la red final se decidirá en el despliegue para optimizar costos y accesibilidad).

*   **Nombre:** SatoshiWasHere
*   **Símbolo:** SWH
*   **Suministro Inicial Total:** 210,000 SWH (Doscientos diez mil)
*   **Decimales:** 18
*   **Estándar:** ERC-20
*   **Blockchain:** EVM Compatible (Ethereum, BNB Chain, Polygon, etc.)
*   **Dirección del Contrato:** [Se publicará tras el despliegue en Mainnet]

### 3.1. Funcionalidades del Contrato Inteligente

El contrato `SatoshiWasHere.sol` implementa las siguientes características:

1.  **ERC-20 Estándar:** Funciones básicas como `transfer`, `approve`, `transferFrom`, `balanceOf`, `totalSupply`.
2.  **Ownable:** Basado en OpenZeppelin, designa una única dirección como propietaria del contrato con privilegios administrativos.
3.  **Pausable:** El propietario puede pausar todas las transferencias de tokens (excepto las del propio propietario) en caso de emergencia o para actualizaciones críticas, y reanudarlas posteriormente.
4.  **Minting Controlado:** Solo el propietario puede acuñar (`mint`) nuevos tokens. El suministro inicial es de 210,000 SWH, acuñados en la creación del contrato a la dirección del propietario.
5.  **Burning:** Cualquier usuario puede quemar (`burn`) sus propios tokens, enviándolos a la dirección `0x...dEaD` y reduciendo el suministro circulante. El propietario también puede quemar tokens desde otras cuentas (`burnFrom`) si tiene la aprobación necesaria.
6.  **Impuesto por Transferencia (Transfer Tax):**
    *   Se aplica un impuesto predeterminado del 2% (`transferTax = 200`) a cada transferencia entre usuarios (excluyendo transferencias desde/hacia el propietario y hacia la dirección de quema).
    *   El monto del impuesto se calcula y se transfiere automáticamente a la dirección de quema (`burnAddress = 0x...dEaD`), logrando un efecto deflacionario.
    *   El propietario puede ajustar este impuesto (`setTransferTax`) hasta un máximo del 10% (`require(tax <= 1000)`).

## 4. Ecosistema SatoshiWasHere

$SWH es más que un token; es el centro de un ecosistema en desarrollo:

1.  **Sitio Web Interactivo:** El portal principal (satoshiwashere.xyz - dominio tentativo) presentará información del token, estadísticas básicas (suministro, quemados, impuesto actual), el whitepaper, roadmap y enlaces a la comunidad. Incorporará elementos visuales y de interacción acordes al tema misterioso.
2.  **Visualizador de Datos (Futuro):** Herramientas para rastrear transacciones, distribución de holders y el impacto de la quema de tokens.
3.  **Muro de Firmas (Futuro):** Una aplicación descentralizada (dApp) donde los holders de $SWH podrán dejar mensajes cortos o firmas en la blockchain, creando un registro permanente de la comunidad.
4.  **Mensajes Ocultos en la Quema (Futuro):** Una interfaz para interpretar o visualizar los datos de las transacciones de quema, buscando patrones o 
