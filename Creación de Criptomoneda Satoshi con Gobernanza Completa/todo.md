## Proyecto Criptomoneda "SatoshiWasHere" ($SWH) - Lista de Tareas

**Fase 1: Planificación y Preparación Inicial**
*   [ ] Crear wallet Web3 (Metamask) - *Usuario debe realizar esta acción externamente.*
*   [x] Configurar IDE de desarrollo (Se usará Remix IDE inicialmente para facilidad, luego se puede migrar a Hardhat si es necesario).
*   [ ] Crear cuenta GitHub - *Usuario debe realizar esta acción externamente.*
*   [ ] Definir estructura del proyecto (crear carpetas para contrato, web, documentos).

**Fase 2: Desarrollo del Ecosistema (Web + Token)**
*   [ ] **Contrato Inteligente (SatoshiWasHere.sol):**
    *   [x] Guardar el código del contrato proporcionado en un archivo `SatoshiWasHere.sol`.
    *   [ ] Verificar dependencias (@openzeppelin/contracts) - *Remix IDE generalmente las maneja automáticamente.*
    *   [ ] Compilar el contrato usando Remix IDE.
    *   [ ] **Probar funcionalidades en Testnet (ej. Sepolia):**
        *   [ ] Obtener ETH de prueba de un Faucet - *Usuario podría necesitar realizar esto o guiarme.*
        *   [ ] Desplegar contrato en Testnet (Sepolia).
        *   [ ] Probar función `mint`.
        *   [ ] Probar función `burn`.
        *   [ ] Probar funciones `pause` y `unpause`.
        *   [ ] Probar función `setTransferTax`.
        *   [ ] Probar transferencias para verificar el impuesto (`transferTax`) y quema (`burnAddress`).
*   [ ] **Sitio Web y Branding:**
    *   [x] Diseñar branding (logo monocromático pixelado, tipografía máquina de escribir, tema misterioso).
    *   [x] Generar estructura básica del sitio web (HTML, CSS, JS).
    *   [x] Desarrollar secciones web:
*           [x] Página principal con información del token (Suministro, decimales, funcionalidades).
        *   [ ] Sección para visualizar supply total, tokens quemados y `transferTax` actual (requiere integración Web3 básica).
*           [x] Crear Roadmap visual (puede ser una imagen o sección HTML).
        *   [ ] *Opcional Avanzado:* Visualizador de holders/transacciones (requiere integración Web3 avanzada y posiblemente API de explorador).
        *   [ ] *Opcional Avanzado:* Muro de firmas para holders (requiere integración Web3 y backend/almacenamiento).
        *   [ ] *Opcional Avanzado:* Interfaz para visualizar tokens quemados como "mensajes ocultos".
    *   [x] Crear Whitepaper (basado en el prompt, en formato Markdown inicialmente, luego se puede convertir a PDF/HTML interactivo).
*   [ ] **Comunidad (Simulada):**
    *   [ ] Crear borradores de contenido para anuncios en Twitter/Discord.

**Fase 3: Preparación para Mainnet**
*   [ ] Obtener fondos (ETH/BNB/MATIC) para gas en Mainnet - *Usuario debe realizar esta acción externamente.*
*   [ ] Finalizar sitio web y prepararlo para despliegue (ej. Vercel/Netlify).
*   [ ] Preparar argumentos y archivos necesarios para la verificación del contrato en el explorador (Etherscan/BscScan/PolygonScan).

**Fase 4: Despliegue y Post-Lanzamiento**
*   [ ] Decidir la red Mainnet (considerando costos: BNB Chain o Polygon recomendadas inicialmente).
*   [ ] Desplegar contrato en la Mainnet elegida.
*   [ ] Guardar y confirmar la dirección del contrato desplegado.
*   [ ] Verificar el código fuente del contrato en el explorador correspondiente.
*   [ ] **(Opcional) Agregar Liquidez en DEX:**
    *   [ ] Elegir DEX (ej. PancakeSwap para BNB Chain, Uniswap para Polygon/Ethereum).
    *   [ ] Guiar al usuario en el proceso de creación del pool de liquidez (SWH/BNB, SWH/MATIC, etc.) - *Usuario debe realizar esta acción externamente.*
*   [ ] **(Opcional) Listado en Plataformas de Seguimiento:**
    *   [ ] Preparar información para solicitar listado en Dextools, Dexscreener, CoinMarketCap, CoinGecko - *Usuario debe realizar esta acción externamente.*
*   [ ] **Monetización:**
    *   [ ] Definir estrategia de venta (whitelist/preventa).
    *   [ ] *Opcional:* Desarrollar contrato y metadatos para NFTs coleccionables.
    *   [ ] *Opcional:* Diseñar/implementar acceso premium para holders.

**Fase 5: Entrega del Proyecto**
*   [ ] Crear un archivo comprimido (.zip) con todos los artefactos del proyecto (código fuente contrato, código fuente web, whitepaper, etc.).
*   [ ] Presentar el proyecto completo y el archivo .zip al usuario.
