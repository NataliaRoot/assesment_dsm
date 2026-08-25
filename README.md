## Reproducibilidad

### Requisitos

* Python 3.12
* Power BI Desktop
* Driver **SQLite ODBC (64 bits)** para que Power BI pueda conectarse a la base SQLite.

### Pasos para ejecutar el proyecto

1. Crear un entorno virtual de Python 3.12.
2. Instalar las dependencias del proyecto:

```bash
pip install -r requirements.txt
```

3. Ejecutar el notebook `notebooks/data_profiling.ipynb`.

   El notebook realiza el proceso ETL y genera automáticamente la base de datos `database/ventas.db`.

4. Instalar el **SQLite ODBC Driver (64 bits)** (solo es necesario la primera vez que se ejecuta el proyecto en un equipo).

5. Abrir `dashboard/Informe de ventas.pbix`.

6. Si Power BI solicita la ruta de la base de datos, seleccionar:

```text
database/ventas.db
```

El dashboard leerá la información directamente desde la base SQLite generada por el pipeline ETL.
