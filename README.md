# Motor de Búsqueda Predictivo

## Descripción

Este proyecto implementa un **motor de búsqueda con sugerencias predictivas** a medida que el usuario escribe. Se compone de una interfaz web moderna y estilizada, que consulta un servicio en **PHP** (`predictivo2.php`) para obtener las predicciones de búsqueda en tiempo real.

## Características

- Interfaz moderna con un diseño limpio y responsivo.
- **Sugerencias en tiempo real** basadas en la entrada del usuario.
- Integración con **PHP y SQL** para obtener predicciones.
- Manejo eficiente de eventos para mejorar la experiencia del usuario.

## Estructura del Proyecto

```bash
├── cliente5.html          # Interfaz principal del buscador
├── styles.css             # Estilos para el diseño del buscador
├── predictivo2.php        # Backend que genera las predicciones
├── neuronal.php           # Archivo adicional para el procesamiento neuronal (si aplica)
├── trespalabras.sql       # Base de datos con palabras clave
```

## Instalación y Configuración

### 1. Requisitos

- **Servidor web con PHP** (Ejemplo: XAMPP, Apache)
- **Base de datos MySQL** para almacenar las palabras clave.
- **Navegador moderno** (Chrome, Firefox, Edge).

### 2. Configuración

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/motor-busqueda.git
   cd motor-busqueda
   ```
2. Importar la base de datos `trespalabras.sql` en MySQL:
   ```sql
   CREATE DATABASE busqueda;
   USE busqueda;
   SOURCE trespalabras.sql;
   ```
3. Configurar `predictivo2.php` para conectar con la base de datos.
4. Iniciar el servidor y abrir `cliente5.html` en el navegador.

## Uso

1. Abrir `cliente5.html`.
2. Escribir una palabra en la barra de búsqueda.
3. Ver las sugerencias en tiempo real.
4. Hacer clic en una sugerencia para autocompletar.

## Tecnologías Utilizadas

- **HTML, CSS y JavaScript** para la interfaz de usuario.
- **PHP** para el procesamiento en el servidor.
- **MySQL** para el almacenamiento de palabras clave.
- **Fetch API** para la comunicación asíncrona entre frontend y backend.

## Mejoras Futuras

- Implementar un algoritmo de aprendizaje para mejorar las predicciones.
- Permitir sugerencias personalizadas basadas en historial de búsqueda.
- Optimizar consultas SQL para mayor eficiencia.

