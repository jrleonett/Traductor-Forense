# Whisper Forense: Transcripción de audios para análisis judicial
![Licencia](https://img.shields.io/badge/Licencia-GNU%20GPL%20v3-blue)
![GitHub](https://img.shields.io/badge/Python-3.8%2B-green)
![GitHub](https://img.shields.io/badge/Estado-Activo-brightgreen)

Este repositorio contiene una implementación especializada del modelo **Whisper de OpenAI**, diseñada para la transcripción precisa de audios en español, con un enfoque en **análisis forense y casos judiciales**. El módulo está optimizado para manejar grabaciones desafiantes, como aquellas con ruido de fondo, acentos regionales o lenguaje coloquial, y ha sido adaptado para incluir funcionalidades avanzadas que lo convierten en una herramienta indispensable para peritos forenses. Desarrollado por **José R. Leonett** para la comunidad de Peritos Forenses Digitales de Guatemala. Más información: www.forensedigital.gt

![Whisper Forense](https://github.com/jrleonett/Traductor-Forense/blob/main/wisperforense.png)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1TJ4AQTrj1LK_8YhdEtRxbj1U0lH6GjeE?usp=sharing)

---

## Características Principales

- **Multilingüe**: Soporte para español y otros idiomas, con énfasis en transcripciones claras y precisas.
- **Robustez**: Capacidad para procesar audios con ruido, distorsiones o baja calidad.
- **Precisión**: Transcripciones de alta calidad, ideales para análisis técnicos y peritajes.
- **Validación**: Siempre se recomienda contrastar las transcripciones con el audio original para garantizar su integridad.
- **Detección de emociones**: Analiza el audio para identificar el estado emocional del hablante (alegría, tristeza, neutral, etc.).
- **Detección de lenguaje violento**: Identifica palabras clave relacionadas con la violencia en el texto transcrito.
- **Traducción a múltiples idiomas**: Permite traducir el texto transcrito a varios idiomas como inglés, portugués, francés, entre otros.
- **Soporte para GPU**: Utiliza la GPU para acelerar el proceso de transcripción.

---

## Beneficios Forenses

Este proyecto ha sido adaptado y mejorado específicamente para su uso en **casos forenses**, donde la precisión y la detección de detalles en los audios son fundamentales. Algunos de los beneficios clave incluyen:

1. **Análisis detallado**: Permite la transcripción y el análisis de audios en contextos judiciales, identificando emociones y lenguaje violento.
2. **Herramienta confiable**: Diseñada para cumplir con los estándares forenses, garantizando la integridad y precisión de los resultados.
3. **Facilidad de uso**: Integra funcionalidades avanzadas en una interfaz sencilla, ideal para peritos forenses y profesionales del ámbito legal.

---

## Requisitos

- **Python 3.7 o superior**.
- **CUDA** (opcional, para usar GPU).
- **Librerías de Python**: `whisper`, `librosa`, `noisereduce`, `googletrans`, `pyannote.audio`, `torch`, `transformers`.

### Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/jrleonett/Traductor-Forense.git
   cd Traductor-Forense

---
## **Uso**

**Preparación del archivo de audio:**
- Coloca tu archivo de audio (en formato MP3, WAV, etc.) en la carpeta transcribir.

**Transcripción del audio:**
- Ejecuta el script de transcripción:
  ```bash
  python transcribir_audio.py
  ```
- El script detectará automáticamente el archivo de audio en la carpeta transcribir y generará un archivo de texto con la transcripción.

**Detección de emociones y lenguaje violento:**
- Durante la transcripción, el script analizará el audio para detectar emociones y lenguaje relacionado con la violencia. Los resultados se mostrarán en la consola y se guardarán en el archivo de texto.

**Traducción a otros idiomas:**
- Después de la transcripción, puedes traducir el texto a otro idioma ejecutando:
  ```bash
  python traducir_texto.py
  
- Selecciona el idioma de destino y el script generará un archivo de texto traducido.

**Descarga del archivo transcrito:**
- El archivo de texto transcrito y traducido se guardará en la carpeta transcribir. Puedes descargarlo manualmente o usar el siguiente comando en Google Colab:
  ```bash
   from google.colab import files
   files.download('ruta/al/archivo.txt')

## **Ejemplo de Uso**
```bash
# Cargar el modelo Whisper
import whisper
model = whisper.load_model("large-v3-turbo", device='cuda')

# Transcribir un archivo de audio
resultado = model.transcribe("ruta/al/audio.mp3", language="es")

# Mostrar el texto transcrito
print(resultado['text'])
```

## **Contribuciones**
¡Las contribuciones son bienvenidas! Si deseas mejorar este proyecto, por favor abre un issue o envía un pull request.

---
# Cómo citar este trabajo.
Usa la siguiente entrada BibTeX si utilizas este trabajo en tu investigación:
```bash
@article{joseRLeonett,
  title={Whisper Forense: Herramienta de Transcripción y Análisis de Audios para Casos Judiciales},
  author={José R. Leonett},
  year={2023},
  url={https://github.com/jrleonett/Traductor-Forense}
}
```

**Licencia.**
- Este proyecto está bajo la licencia GNU General Public License v3.0. Consulta el archivo LICENSE para más detalles.

