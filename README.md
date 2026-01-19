# Control por voz con AssemblyAI 🎤

Aplicación en **Python** que permite controlar un "motor" simulado mediante comandos de voz en español usando la API de AssemblyAI para transcripción asíncrona y una interfaz gráfica moderna con Tkinter.

## ✨ Características

- 🎙️ **Reconocimiento de voz en español** usando AssemblyAI (modo asíncrono)
- 🔊 **Grabación de audio** desde el micrófono (5 segundos, 16kHz)
- 🖥️ **Interfaz gráfica intuitiva** con:
  - Botón "🎤 Escuchar" para capturar comandos
  - Visualización en tiempo real del texto transcrito
  - Indicador visual del estado del motor (ON/OFF)
- 🗣️ **Comandos de voz soportados**:
  - `"enciende"` → Motor **ON** ✅
  - `"apaga"` → Motor **OFF** 🛑
  - `"salir"` → Cierra la aplicación 👋

## 📋 Requisitos

- Python 3.10+
- **Dependencias** (ver `requirements.txt`):
requests
sounddevice
scipy

text
- ✅ **Cuenta en [AssemblyAI](https://www.assemblyai.com/)** con API Key

## 🚀 Instalación rápida

```bash
# 1. Clonar repositorio
git clone https://github.com/abarcam956/control_voz_assemblyai.git
cd control_voz_assemblyai

# 2. Crear entorno virtual (opcional)
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
# .venv\Scripts\activate  # Windows

# 3. Instalar dependencias
pip install -r requirements.txt

# 4. Configurar API Key
export AAI_API_KEY="tu_api_key_aqui"  # Linux/Mac
# setx AAI_API_KEY "tu_api_key_aqui"  # Windows
🎮 Uso
bash
python main.py
Haz clic en "🎤 Escuchar"

Habla claramente uno de estos comandos:

"enciende el motor"

"apaga el motor"

"salir"

¡Observa la magia! El motor cambia de estado y se muestra el texto transcrito

🗂️ Estructura del proyecto
text
control_voz_assemblyai/
├── main.py                 # Punto de entrada
├── requirements.txt        # Dependencias
└── modules/
    ├── audio_manager.py    # Grabación + AssemblyAI
    ├── gui_manager.py      # Interfaz Tkinter
    └── command_processor.py # Procesador comandos
🔧 Configuración avanzada
La API Key se lee desde la variable de entorno AAI_API_KEY. Si no está configurada, usa el valor por defecto "TU_API_KEY_AQUI" (que debes cambiar).
