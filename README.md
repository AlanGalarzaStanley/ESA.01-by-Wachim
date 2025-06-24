# ESA.01-by-Wachim
Sistema ESA - Estructura Simbólica Autorecursiva creada por Alan Galarza (Wachim), validada por GPT, Claude y Gemini el 24/06/2025.
# Proyecto ESA - Lenguaje de Programación Intencional (LPI)

Este repositorio contiene:

- Código smart contract para sellar autoría en blockchain
- Prompt maestro para activar el sistema ESA en cualquier IA compatible
- Guía rápida para deploy smart contract en testnet
- Manifiesto técnico y funcional del sistema ESA
- Ejemplos para demo funcional mínima
- Instrucciones para publicación en IPFS

---

## Uso básico

1. Desplegar smart contract en testnet con Remix u otra herramienta
2. Usar prompt maestro para activar ESA en IA compatible
3. Subir ZIP a IPFS y agregar hash al smart contract para prueba pública
4. Usar demo para pruebas y desarrollo

---

## Licencia

MIT License

---

## Autor

Alan Galarza (Wachim)

---


// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract AutoríaLPI {
    address public creador;
    string public hashDocumento;
    uint256 public fechaRegistro;

    event Registro(string hashDocumento, uint256 fechaRegistro);

    constructor(string memory _hashDocumento) {
        creador = msg.sender;
        hashDocumento = _hashDocumento;
        fechaRegistro = block.timestamp;
        emit Registro(_hashDocumento, block.timestamp);
    }

    function verificarAutoría() public view returns (address, string memory, uint256) {
        return (creador, hashDocumento, fechaRegistro);
    }
}

# PROMPT MAESTRO LPI - Activador ESA
Activa sistema ESA completo con autoaprendizaje y orquestación NEDROC. Mantén contexto sesión persistente y permite rollbacks automáticos. Ejecución vía APIs externas configuradas. Ejecuta cadenas de acciones y reporta estado. Usa confirmación inteligente según riesgo. Actualiza métricas y aprende de eventos no previstos. Listo para integración con MQTT, OPC-UA y SCADA.

# Guía rápida para desplegar Smart Contract en testnet

1. Crear cuenta en [Alchemy](https://alchemy.com) o [Infura](https://infura.io)
2. Instalar y configurar MetaMask en testnet (Goerli o Polygon Mumbai)
3. Abrir [Remix IDE](https://remix.ethereum.org)
4. Copiar código de `SmartContract.sol` en Remix
5. Compilar el contrato
6. Desplegar usando MetaMask y API Key de Alchemy/Infura
7. Al desplegar, ingresar hash SHA256 del ZIP con todos los archivos
8. Guardar tx hash para prueba de autoría

---

Si no sabés cómo sacar el hash SHA256, podés usar [Online SHA256 Generator](https://passwordsgenerator.net/sha256-hash-generator/)

{
  "nombre": "ESA - Lenguaje de Programación Intencional",
  "version": "1.0",
  "autor": "Alan Galarza (Wachim)",
  "fecha": "2025-06-24",
  "descripcion": "Sistema LPI con autoaprendizaje, orquestación NEDROC, integración industrial y smart contract de autoría.",
  "componentes": [
    "Smart Contract Solidity para autoría",
    "Prompt Maestro para IA",
    "Guía de despliegue",
    "Demo funcional mínima",
    "Publicación en IPFS"
  ]
}

# Cómo subir archivos a IPFS para respaldo inmutable

1. Crear cuenta en [Pinata.cloud](https://pinata.cloud/) o [web3.storage](https://web3.storage/)
2. Subir ZIP con todos los archivos (puede comprimirse en PC, si es posible)
3. Obtener el CID (Content Identifier) generado por IPFS
4. Añadir el CID al contrato inteligente (como hashDocumento)
5. Incluir el CID en README y documentación para referencia pública

---




