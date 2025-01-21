# 🔧 Configuración del Entorno Virtual - Proyecto de Segmentación

<div align="center">

![Python Version](https://img.shields.io/badge/Python-3.12-blue.svg)
![VSCode](https://img.shields.io/badge/IDE-VS%20Code-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

</div>

## 📋 Contenido
- [Requisitos Previos](#requisitos-previos)
- [Configuración del Entorno](#configuración-del-entorno)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Solución de Problemas](#solución-de-problemas)
- [Notas Importantes](#notas-importantes)

## ⚡ Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- ✅ Python 3.12
- ✅ Visual Studio Code
- ✅ PowerShell
- ✅ Extensión de Python para VSCode

## 🚀 Configuración del Entorno

### 1. Crear y Activar el Entorno Virtual

```powershell
# Eliminar entorno virtual existente (si existe)
Remove-Item -Recurse -Force .venv

# Crear nuevo entorno virtual
python -m venv .venv

# Activar el entorno virtual
.\.venv\Scripts\Activate
```

### 2. Actualizar Herramientas Base

```powershell
# Actualizar pip
python -m pip install --upgrade pip

# Instalar setuptools y wheel
pip install --upgrade setuptools wheel
```

### 3. Instalar Dependencias

```powershell

# Instalar desde requirements.txt
pip install -r requirements.txt
```
Esto puede tardar un rato, espere a que termine.

### 4. Configurar Jupyter en VSCode

1. 📁 Abrir VSCode en la carpeta del proyecto
2. 📓 Abrir un archivo `.ipynb` (notebook)
3. ⚙️ Configurar el kernel:
   - Hacer clic en "Select Kernel"
   - Buscar el kernel con '.venv'
   - Si no aparece → "+ Python Environments..."
   - Seleccionar el entorno virtual creado

### 5. Verificar la Instalación

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
from skimage import segmentation

print("✨ Todas las dependencias están correctamente instaladas")
```

## 📁 Estructura del Proyecto

```
proyecto_segmentacion/
│
├── 🔧 .venv/                # Entorno virtual
├── 📝 requirements.txt     # Lista de dependencias
├── 📘 README.md           # Documentación del proyecto
├── 📸 images/             # Imágenes originales
├── ✅ ground_truth/       # Ground truths
├── 📓 notebooks/          # Notebooks de Jupyter
└── 📊 results/            # Resultados
```

## ❗ Solución de Problemas

### 1. Kernel No Visible en Jupyter

```powershell
pip install --upgrade ipykernel
python -m ipykernel install --user --name=nombre_entorno
```

### 2. Problemas con Dependencias

```powershell
cd .\entorno\
pip install --upgrade -r requirements.txt
```

### 3. VSCode No Reconoce el Entorno
1. Cerrar VSCode completamente
2. Reabrir VSCode
3. Seleccionar el intérprete de Python del entorno virtual

## 📌 Notas Importantes

> ⚠️ **Puntos Clave**

- ✅ Verificar que el entorno virtual está activado `(.venv)`
- 📝 `requirements.txt` se encuentra en `entorno/`
- 🔄 Mantener el entorno virtual actualizado
- ❌ No subir `.venv/` al control de versiones
- 🔧 Ante problemas, es seguro eliminar y recrear el entorno
- 🎯 Asegurar la selección del kernel correcto en notebooks

---

<div align="center">

**¿Necesitas ayuda?** [Abrir un Issue](https://github.com/eni2910/evaluacion-de-segmentacion/issues)

</div>