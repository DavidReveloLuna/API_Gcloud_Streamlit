# API_Gcloud_Streamlit
Generaremos un modelo SVM y lo pondremos en producción usando Streamlit y Google Cloud. El modelo SVM permitirá recomendar un tipo de cultivo dependiendo de características del suelo y ambientales.

##  1. Entrenamiento del modelo
Entrenamos el modelo SVM usando el siguiente cuaderno de colab
    
   [CropPrediction.ipynb](https://github.com/DavidReveloLuna/API_Gcloud_Streamlit/blob/master/CropPrediction.ipynb)

##  2. Producción en servidor local - preparación del entorno

Creamos un entorno con python 3.7, e instalamos las dependencias necesarias.

    $   conda create -n ApiCrop
    $   conda activate ApiCrop
    $   conda install python=3.7
    $   pip install -r requirements.txt
    $   streamlit run app.py
    
##  3. Producción en servidor remoto

    *   Activar una cuenta en google cloud
    *   Crear proyecto en google cloud
    *   Instalar GoogleCloudSDK
        (https://cloud.google.com/sdk/docs/install)
    *   Ejecutar en la terminal:
    
    $ gcloud init
    $ gcloud app deploy app.yaml --project "Nombre del proyecto"
    
    
  ![Screenshot](https://github.com/DavidReveloLuna/API_Gcloud_Streamlit/blob/master/assets/Screenshot.png)

## Agradecimientos

[Praneeth Kandula](https://medium.com/analytics-vidhya/deploying-streamlit-apps-to-google-app-engine-in-5-simple-steps-5e2e2bd5b172)
