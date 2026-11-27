# Gestion de Productos - CRUD en Python

[![CI - Pruebas unitarias](https://github.com/estebanrico1131064/EstebanRicoCorrales1013457626/actions/workflows/ci.yml/badge.svg)](https://github.com/estebanrico1131064/EstebanRicoCorrales1013457626/actions/workflows/ci.yml)

Proyecto de la Guia de Trabajo No. 5 de **Aplicaciones y Servicios Web**
(Instituto Tecnologico Metropolitano).

Aplicacion de consola que implementa las operaciones **Crear, Leer, Actualizar y
Eliminar** sobre un registro de productos, con persistencia en un archivo JSON y
pruebas unitarias con `unittest`. Incluye un flujo de CI/CD con GitHub Actions que
ejecuta las pruebas automaticamente en cada `push`.

## Requisitos

- Python 3.10 o superior

## Estructura del proyecto

```
.
|-- main.py                     # Menu interactivo (punto de entrada)
|-- crud/
|   |-- __init__.py             # Expone las clases publicas del paquete
|   |-- modelo.py               # Entidad Producto
|   |-- almacenamiento.py       # Persistencia JSON
|   |-- servicio.py             # Logica CRUD y validaciones
|   `-- errores.py              # Excepciones del dominio
|-- tests/
|   |-- __init__.py
|   |-- test_crud.py            # Pruebas del CRUD
|   `-- test_cli.py             # Pruebas del menu de consola
|-- data/
|   `-- .gitkeep
|-- .github/workflows/
|   `-- ci.yml                  # Flujo CI/CD con GitHub Actions
|-- requirements.txt
`-- README.md
```

## Uso

```bash
python main.py
```

## Pruebas unitarias

```bash
python -m unittest discover -s tests -v
```

## CI/CD

El workflow `.github/workflows/ci.yml` se ejecuta automaticamente en cada `push` y en
cada `pull_request` sobre la rama `main`. El flujo clona el repositorio, configura
Python, instala dependencias y ejecuta las pruebas unitarias con reporte de cobertura.

## Autor

Esteban Rico Corrales - [estebanrico1131064](https://github.com/estebanrico1131064)

Repositorio: <https://github.com/estebanrico1131064/EstebanRicoCorrales1013457626>
