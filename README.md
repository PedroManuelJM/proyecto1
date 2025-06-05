# Clasificador de Comentarios - API con FastAPI y HuggingFace 🤖🚀

Este proyecto es una API creada con FastAPI que clasifica comentarios de texto utilizando un modelo de Hugging Face.

## 🧠 Modelo usado
Modelo: `pedrojm/modelv2_clasificacioncomentario`  
Pipeline: `text-classification` usando `transformers`

## 🚀 Cómo usar

### 1. Clonar el repositorio

2. Crear entorno virtual e instalar dependencias

py -3.10 -m venv venv310
venv310\Scripts\activate
pip install -r requirements.txt

3. Configurar variable de entorno
Crea un archivo .env con tu token de Hugging Face:

HF_TOKEN=tu_token_aqui

4. Ejecutar la API
python app.py

5. Probar la API

http://0.0.0.0:7860/  

GET /
Respuesta: {"message": "API funcionando. Usa POST en /predict para clasificar un comentario."}

http://0.0.0.0:7860/predict 
POST /predict
Body:

json
Copiar
Editar
{
  "text": "Me encantó el producto"
}

🧪 Tests
Puedes correr pruebas con:
pytest test.py



📦 Requisitos
Python 3.10+

FastAPI

Transformers

Torch

HuggingFace Hub

Uvicorn

Python-dotenv