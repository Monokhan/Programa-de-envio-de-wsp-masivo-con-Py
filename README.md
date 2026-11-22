<div align="center">

<img src="assets/banner.svg" width="100%" alt="WhatsApp masivo con Python"/>

<br/>

<img src="https://img.shields.io/badge/Python-0b1220?style=for-the-badge&logo=python&logoColor=22d3ee" alt="Python"/>
<img src="https://img.shields.io/badge/Selenium-0b1220?style=for-the-badge&logo=selenium&logoColor=5fd4a8" alt="Selenium"/>
<img src="https://img.shields.io/badge/pandas-0b1220?style=for-the-badge&logo=pandas&logoColor=a78bfa" alt="pandas"/>
<img src="https://img.shields.io/badge/WhatsApp_Web-0b1220?style=for-the-badge&logo=whatsapp&logoColor=25d366" alt="WhatsApp Web"/>

</div>

Bot en Jupyter que **envía mensajes personalizados por WhatsApp Web** a una lista de contactos tomada de Excel. Además de texto, puede adjuntar **imágenes, videos y documentos**. Controla el navegador con Selenium, igual que si una persona escribiera cada mensaje.

## ⚙️ Cómo funciona

```
contactos.xlsx + llaves.xlsx ──► pandas ──► Selenium abre WhatsApp Web ──► mensaje + adjuntos a cada número
```

| Etapa del notebook | Qué hace |
|---|---|
| **Carga de datos** | Lee los contactos y arma el número con su código de país |
| **Envío de mensajes** | Abre el chat de cada contacto y envía el texto |
| **Imágenes y videos** | Usa el botón *Adjuntar* y el selector de multimedia |
| **Documentos** | Adjunta archivos como PDF |

## 📁 Archivos de entrada

| Archivo | Columnas |
|---|---|
| `contactos.xlsx` (lo creas tú) | `cel` y `codigo_pais` |
| `llaves.xlsx` | `mensaje`, `ruta_imagen`, `ruta_video`, `ruta_documento` |

Los archivos adjuntos deben estar en la misma carpeta del notebook.

## 🚀 Cómo usarlo

1. Instala Selenium y pandas: `pip install selenium pandas openpyxl`.
2. Descarga **ChromeDriver** en la misma versión de tu Chrome (Chrome → ⋮ → Ayuda → Información de Google Chrome).
3. Prepara `contactos.xlsx` y `llaves.xlsx`, abre el notebook y escanea el código QR de WhatsApp Web.
4. Si WhatsApp cambia su interfaz y el botón de enviar deja de funcionar, actualiza su XPath copiándolo desde el inspector del navegador.

> **Uso responsable:** envía mensajes solo a personas que aceptaron recibirlos y no acortes los tiempos de espera entre envíos. WhatsApp puede bloquear los números que envían mensajes masivos no solicitados.

## 🧭 Próximas mejoras

- Interfaz gráfica.
- Reporte en Excel con los números enviados y los que no tienen WhatsApp.

```
├── Programa de envios_masivo_WSP_ByMonokhan.ipynb   ← bot
├── llaves.xlsx                                      ← mensaje y rutas de adjuntos
├── Readme.txt                                       ← notas originales
└── assets/                                          ← banner de este README
```

---

<div align="center">

Hecho por **[Marcelo Reinoso](https://github.com/Monokhan)** · datos aplicados a minería e infraestructura

</div>
