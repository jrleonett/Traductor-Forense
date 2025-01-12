# Whisper: Traducción y conversión de audios en español a texto

**Whisper** es una red neuronal desarrollada por OpenAI ([ver más](https://openai.com/blog/whisper/)) que convierte el habla en texto con una precisión cercana a la humana. Este proyecto utiliza Whisper para transcribir audios en español, incluso en situaciones con ruido de fondo, acentos o jerga. 

Whisper es un sistema de reconocimiento de voz (ASR) entrenado con 680.000 horas de datos multilingües, lo que lo hace robusto y adaptable a diferentes contextos. Además de la transcripción, Whisper puede traducir audios a otros idiomas, como el inglés.

Este proyecto ha sido adaptado y mejorado para su uso en casos forenses, donde la precisión y la detección de detalles son cruciales. Se han incorporado funcionalidades adicionales, como:

- **Detección de emociones**: Identifica el estado emocional del hablante (alegría, tristeza, neutral, etc.).
- **Detección de lenguaje violento**: Reconoce palabras o frases relacionadas con violencia en el texto transcrito.

Estas mejoras lo convierten en una herramienta poderosa para la transcripción de audios en contextos judiciales y forenses.

---

![image](https://user-images.githubusercontent.com/41134438/192058743-526e2dcc-da77-4ec4-8259-26b222c0768a.png)
---
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1TJ4AQTrj1LK_8YhdEtRxbj1U0lH6GjeE?usp=sharing)

## Características Principales
- **Transcripción de audio a texto**: Convierte archivos de audio (MP3, WAV, etc.) en texto en español.
- **Detección de emociones**: Analiza el audio para detectar emociones como alegría, tristeza, neutral, etc.
- **Detección de lenguaje violento**: Identifica palabras clave relacionadas con la violencia en el texto transcrito.
- **Traducción a múltiples idiomas**: Permite traducir el texto transcrito a varios idiomas como inglés, portugués, francés, entre otros.
- **Soporte para GPU**: Utiliza la GPU para acelerar el proceso de transcripción.

## Requisitos
- Python 3.7 o superior.
- CUDA (opcional, para usar GPU).
- Librerías de Python: `whisper`, `librosa`, `noisereduce`, `googletrans`, `pyannote.audio`, `torch`, `transformers`.

## Instala las dependencias necesarias:
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tuusuario/traductor-whisper.git
   cd traductor-whisper

2. Instala Whisper:
   ```bash
   pip install git+https://github.com/openai/whisper.git

3. Asegúrate de tener una GPU compatible con CUDA si deseas acelerar el proceso de transcripción.
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
@article{joséRLeonett,
  title={Whispers, traductor y convertidor de audios en español a escritura},
  author={José R. Leonett},
  year={2023}
}
```

**Licencia.**
- Este proyecto está bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.

