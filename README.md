# Instrucciones de Configuración y Ejecución

## 1. Crear el entorno virtual con Python 3.11

```bash
C:\Python313\python.exe -m venv venv
```

## 2. Activar el entorno virtual

```bash
.\venv\Scripts\activate
```

## 3. Instalar las dependencias

```bash
pip install -r requirements.txt
```

## 4. Instalar Playwright

```bash
playwright install
```

## 5. Ejecutar el archivo SQL en PostgreSQL

### En Windows

```bash
psql -d mef -U postgres -f consulta_ejecucion_gasto.sql
```

### En Linux

```bash
su postgres
psql -d mef -f consulta_ejecucion_gasto.sql
```

## 6. Configurar y ejecutar los scripts Python

Editar la cadena de conexión en los siguientes archivos:

- `departamentos.py`
- `provincias3.py`
- `distritos3.py`

Luego ejecutar:

```bash
cd .\apps
python departamentos.py
```

---

**Nota:** Asegúrese de que PostgreSQL esté en ejecución y que la base de datos `mef` exista antes de ejecutar el script SQL.
