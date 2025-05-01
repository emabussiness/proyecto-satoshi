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

mensajes" ocultos en la actividad de la red.
5.  **NFTs Coleccionables (Opcional):** Una colección limitada de 21 NFTs, cada uno representando una frase críptica o un concepto relacionado con Satoshi y el origen de Bitcoin. Estos NFTs podrían otorgar beneficios adicionales dentro del ecosistema.

## 5. Roadmap: Fases del Misterio

Nuestro camino se despliega en fases, cada una construyendo sobre la anterior:

*   **Fase 1: Génesis (Completada)**
    *   Conceptualización del proyecto.
    *   Desarrollo y auditoría interna del contrato inteligente `SatoshiWasHere.sol`.
    *   Creación de la identidad visual y branding.
    *   Desarrollo inicial del sitio web y whitepaper.
*   **Fase 2: Despliegue y Establecimiento (Actual)**
    *   Pruebas exhaustivas del contrato en Testnet (Sepolia/Goerli).
    *   Selección de la red Mainnet (priorizando BNB Chain o Polygon por eficiencia).
    *   Despliegue oficial del contrato en Mainnet.
    *   Verificación del código fuente en el explorador correspondiente (Etherscan/BscScan/PolygonScan).
    *   Lanzamiento del sitio web oficial v1.
*   **Fase 3: Liquidez y Visibilidad**
    *   Creación del pool de liquidez inicial en un DEX principal (ej. PancakeSwap, Uniswap).
    *   Bloqueo de una porción de la liquidez (opcional, para generar confianza).
    *   Solicitud de listado en plataformas de seguimiento (CoinGecko, CoinMarketCap, Dextools, Dexscreener).
    *   Inicio de campañas de marketing y construcción de comunidad (Twitter, Discord).
*   **Fase 4: Expansión del Ecosistema**
    *   Desarrollo e implementación del "Muro de Firmas" para holders.
    *   Creación del visualizador de datos on-chain.
    *   Investigación y posible lanzamiento de la colección de NFTs "21 Misterios".
    *   Exploración de integraciones o utilidades adicionales para $SWH.
*   **Fase 5: Consolidación y Futuro Desconocido**
    *   Evaluación de la gobernanza comunitaria.
    *   Desarrollo continuo basado en el feedback de la comunidad.
    *   Revelación de nuevos "misterios" o funcionalidades.

## 6. Monetización y Distribución Inicial

El objetivo principal no es la monetización agresiva, sino la creación de un proyecto sostenible y enigmático. Las estrategias consideradas incluyen:

*   **Asignación del Propietario:** El suministro inicial de 210,000 SWH se acuña a la dirección del propietario. Una parte significativa se destinará a:
    *   Provisión de liquidez inicial en DEX.
    *   Fondos para marketing y desarrollo futuro.
    *   Airdrops o recompensas comunitarias.
    *   Tesorería del proyecto.
*   **Venta Inicial (Opcional):** Se podría considerar una pequeña preventa o venta por whitelist para recaudar fondos iniciales y distribuir tokens a los primeros adoptantes.
*   **NFTs Coleccionables:** Si se implementa la colección de NFTs, su venta podría generar ingresos para el proyecto.
*   **Acceso Premium (Futuro):** Ciertas funcionalidades avanzadas del ecosistema o contenido exclusivo podrían requerir holding de $SWH o NFTs específicos.

La transparencia en la asignación de fondos será comunicada a la comunidad.

## 7. Riesgos y Consideraciones

Invertir en $SWH, como en cualquier criptomoneda, implica riesgos:

*   **Volatilidad del Mercado:** El precio de $SWH puede fluctuar significativamente.
*   **Riesgos del Contrato Inteligente:** Aunque se toman precauciones, los bugs o vulnerabilidades son siempre un riesgo inherente.
*   **Riesgos Regulatorios:** El panorama regulatorio de las criptomonedas está en constante evolución.
*   **Dependencia del Propietario (Inicial):** La naturaleza `Ownable` del contrato implica confianza en el equipo fundador en las etapas iniciales.
*   **Adopción y Comunidad:** El éxito del proyecto depende de la adopción y participación activa de la comunidad.

## 8. Conclusión: Únete a la Búsqueda

SatoshiWasHere ($SWH) es más que código y especulación. Es una invitación a participar en un experimento narrativo y tecnológico. Es un lienzo digital donde la comunidad puede dejar su propia marca, inspirada por el misterio más grande de la criptografía. No ofrecemos respuestas definitivas, solo un espacio para explorar, especular y construir juntos.

El viaje apenas comienza. Las claves están ocultas a simple vista. ¿Estás listo para buscar?

## 9. Comunidad y Contacto

*   **Sitio Web:** [Dirección del sitio web]
*   **Twitter:** [Enlace a Twitter]
*   **Discord:** [Enlace a Discord]
*   **GitHub:** [Enlace al Repositorio GitHub]
*   **Contrato (Mainnet):** [Dirección del contrato una vez desplegado]

---
