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


# Análisis de `neuronal.php`

El archivo `neuronal.php` implementa un sistema de **texto predictivo neuronal** basado en una interfaz web interactiva. Su funcionamiento se divide en varias partes:

## 1. Estructura General
- Es una página web con **HTML, CSS y JavaScript**.
- Contiene un **cuadro de texto** donde el usuario escribe.
- Muestra **sugerencias de palabras** basadas en el texto ingresado.
- Representa visualmente **neuronas activadas** según las letras escritas.

## 2. Interfaz Visual
- Usa **CSS** para diseñar una interfaz oscura con texto en blanco.
- Las **neuronas** (representadas como círculos) cambian de color cuando el usuario escribe.
- Al escribir, se activa la función de predicción, mostrando palabras sugeridas en una lista.

## 3. Funcionamiento del Sistema de Predicción
Cada vez que el usuario **escribe una palabra**, el sistema:
1. Toma las **dos últimas palabras** escritas.
2. Envía una **petición a un archivo externo (`predictivo2.php`)** para obtener predicciones.
3. **Recibe las palabras sugeridas** desde el backend.
4. Muestra las palabras en una lista para que el usuario pueda seleccionarlas.

## 4. Activación de Neuronas
- Cada letra escrita **activa una "neurona" virtual** en pantalla.
- Las neuronas son pequeños **círculos** que cambian de color cuando su letra correspondiente es usada.
- Esto **simula una red neuronal activándose en tiempo real**.

## 5. Conexión con `predictivo2.php`
- El archivo no incluye la **lógica de predicción** dentro de `neuronal.php`, sino que **depende de `predictivo2.php`**.
- `predictivo2.php` recibe la entrada del usuario y devuelve las palabras más probables para completar la frase.

---

## ¿Cómo funciona en términos prácticos?
1. El usuario **escribe en el cuadro de texto**.
2. El sistema toma las **últimas dos palabras** escritas.
3. Se hace una **petición a `predictivo2.php`** para obtener palabras sugeridas.
4. Si hay predicciones, aparecen en una lista debajo del cuadro de texto.
5. Al hacer clic en una sugerencia, se añade al texto automáticamente.
6. Se **actualizan las "neuronas activas"** visualmente con las letras ingresadas.

---

## ¿Falta algo importante?
- No se puede analizar `predictivo2.php`, que es la parte que realmente **hace la predicción**.
- Si `predictivo2.php` usa una **red neuronal real**, sería importante revisar cómo procesa los datos.

---

## Conclusión
 **Este archivo es solo la interfaz visual** y la lógica de interacción. La verdadera inteligencia del sistema depende de `predictivo2.php`, que maneja la predicción del texto basado en modelos estadísticos o redes neuronales.

Si quieres que analice `predictivo2.php`, súbelo y lo reviso. 

