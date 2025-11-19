💱 Conversor de Monedas con Historial en Java:
Este proyecto es una aplicación de consola desarrollada en Java que permite convertir entre distintas monedas utilizando una API externa. Además, registra cada conversión en un archivo historial.json para su posterior consulta.

🚀 Funcionalidades:
- Conversión de monedas en tiempo real usando la API de ExchangeRate-API.
- Menú interactivo para seleccionar moneda base, destino y monto.
- Registro automático de cada conversión en un archivo JSON.
- Visualización del historial de conversiones al finalizar el programa.
- Arquitectura modular con separación por paquetes y responsabilidades.

🧱 Estructura del proyecto:
CHALLENGE 2/
├── src/
│   ├── principal/
│   │   └── Principal.java
│
│   ├── conversores/
│   │   ├── ListaCodigos.java
│   │   ├── MainConversor.java
│   │   ├── MonedasParaConvertir.java
│   │   └── TasaDeConversiones.java
│
│   ├── historial/
│   │   ├── CosasParaConvertir.java
│   │   └── ManejoHistorial.java
│
│   ├── http/
│   │   └── ClienteHttp.java
│
│   ├── interfaces/
│   │   └── PasajeRecordNumero.java
│
│   ├── linkApi/
│   │   └── LinkApi.java
│
│   ├── menuConversor/
│   │   └── MensajeIncial.java
│
│   └── excepciones/
│       ├── MonedaNoSoportadaExcepcion.java
│  
│
├── .gitignore
├── README.md     └── InvocacionDeMetodoExcepcion.java


📂 Clases y responsabilidades
- Principal: flujo principal de ejecución.
- ListaCodigos: lista fija de monedas disponibles.
- MainConversor: realiza la conversión usando tasas.
- MonedasParaConvertir: record con tasas por moneda.
- TasaDeConversiones: mapea el JSON de la API.
- CosasParaConvertir: representa una conversión.
- ManejoHistorial: gestiona el historial en JSON.
- ClienteHttp: realiza la solicitud HTTP.
- PasajeRecordNumero: obtiene la tasa usando reflexión.
- LinkApi: centraliza la URL base y el Gson formateado.
- MensajeIncial: contiene los mensajes del menú.
- MonedaNoSoportadaExcepcion: error por moneda inválida.
- InvocacionDeMetodoExcepcion: error al invocar métodos por reflexión.

🛠 Requisitos
- Java 17 o superior
- Conexión a Internet
- Biblioteca externa: Gson

📄 Ejemplo de historial generado
[
  {
    "monedaBase": "ARS",
    "monedaDestino": "USD",
    "montoOriginal": 10000.0,
    "montoConvertido": 60.28,
    "fecha": "2025-11-19"
  }
]


⚠️ Este archivo se guarda como historial.json y está excluido del repositorio mediante .gitignore.


🧠 Detalles técnicos
- API usada: ExchangeRate-API
- Reflexión en Java: se usa para acceder dinámicamente a métodos del record MonedasParaConvertir.
- Persistencia: el historial se guarda en JSON usando Gson.
- Diseño modular: cada responsabilidad está separada en su propio paquete.


📬 Contacto
Desarrollado por Pablo Cabrera como parte del curso de Practicando con Java: Challenge Conversor de Monedas, que forma parte del plan de estudios ONE | TECH FOUNDATION - Especialización Back-End que brinda la sociedad entre Oracle y Alura Latam.



https://github.com/user-attachments/assets/a109ac6b-91bb-4b3c-830c-c0c772cb6594

