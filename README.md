## Getting Started

### Prerequisites

- Python >= 3.12
- [Poetry](https://python-poetry.org/docs/#installation)
- Git
- Cuenta de GitHub

### Create Your Repository

Antes de comenzar, cada estudiante deberá crear un **repositorio personal en GitHub** para desarrollar y mantener su solución.

Desde GitHub, seleccionar **New repository** y configurar:

- **Repository name:** elegir un nombre identificativo para el caso práctico.
- **Add README:** activar la opción para generar automáticamente un `README.md`.
- **Add .gitignore:** seleccionar la plantilla **Python**.

### GitHub Authentication

**Importante:** una vez creado el repositorio, cada estudiante deberá generar un nuevo **Personal Access Token (PAT)** con acceso a su repositorio personal.

Seguir las instrucciones disponibles en la guía oficial de la asignatura:

[GitHub Authentication Guide](https://github.com/UAX-VCMT-26-27/.github/blob/main/authentication/README.md)

No compartir el token ni incluirlo en archivos del proyecto.

### Clone Your Repository

Clonar el repositorio personal recién creado:

```bash
git clone https://github.com/TU_USUARIO/TU_REPOSITORIO.git
cd TU_REPOSITORIO
```

Sustituir `TU_USUARIO` y `TU_REPOSITORIO` por los valores correspondientes.

Para configurar la autenticación y la identidad de Git, seguir la guía indicada anteriormente.

### Copy Case Study Materials

Los materiales iniciales están disponibles en el [repositorio oficial del caso práctico](https://github.com/UAX-VCMT-26-27/aa-case-02-oil-price-prediction).

Desde la raíz del repositorio personal, ejecutar:

```bash
git clone --depth 1 https://github.com/UAX-VCMT-26-27/aa-case-02-oil-price-prediction.git /tmp/aa-case-02-materials

cp -a /tmp/aa-case-02-materials/docs ./
cp -a /tmp/aa-case-02-materials/scripts ./
cp /tmp/aa-case-02-materials/pyproject.toml ./
cp /tmp/aa-case-02-materials/poetry.lock ./
cp /tmp/aa-case-02-materials/.gitattributes ./

rm -rf /tmp/aa-case-02-materials
```

Estos comandos copian el enunciado, los scripts y los archivos de configuración necesarios.

**Importante:** se conservan el `README.md` y el `.gitignore` generados al crear el repositorio personal. Cada estudiante deberá completar su README con la documentación de su solución.

### Install Dependencies

Desde la raíz del repositorio:

```bash
poetry install
```

### Download Data

Ejecutar el script proporcionado:

```bash
poetry run python scripts/download_data.py
```

El script descarga datos históricos del petróleo Brent y WTI, junto con indicadores económicos y financieros, desde FRED y Yahoo Finance.

El dataset se guardará automáticamente en:

```text
data/petroleo_dataset.csv
```

### Upload Your Work

Para guardar los materiales iniciales en GitHub:

```bash
git add .
git commit -m "chore: add case study materials and project configuration"
git push origin main
```

## Case Study

El enunciado completo y los requisitos de entrega están disponibles en:

[`docs/caso_uso_petroleo.pdf`](docs/caso_uso_petroleo.pdf)

---

**Nota:** Cada estudiante deberá desarrollar su propia solución, documentarla en el README y mantener todo el código en su repositorio personal.
