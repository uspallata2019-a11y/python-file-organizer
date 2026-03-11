import os
import shutil

carpeta = "Descargas"

for archivo in os.listdir(carpeta):
    ruta = os.path.join(carpeta, archivo)

    if archivo.endswith(".jpg") or archivo.endswith(".png"):
        destino = os.path.join(carpeta, "Imagenes")
        os.makedirs(destino, exist_ok=True)
        shutil.move(ruta, destino)

    elif archivo.endswith(".pdf"):
        destino = os.path.join(carpeta, "Documentos")
        os.makedirs(destino, exist_ok=True)
        shutil.move(ruta, destino)
