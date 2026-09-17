# Source: https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda

Tabla de Contenidos

- [1\. Conceptos Fundamentales: Conda vs. Anaconda](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#1-conceptos-fundamentales-conda-vs-anaconda)
- [2\. Gestión de Paquetes (Packages)](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#2-gesti%c3%b3n-de-paquetes-packages)
 - [Comandos Esenciales de Paquetes](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#comandos-esenciales-de-paquetes)
- [3\. Canales (Channels)](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#3-canales-channels)
- [4\. Gestión de Ambientes (Environments)](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#4-gesti%c3%b3n-de-ambientes-environments)
 - [Flujo de trabajo con Ambientes](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#flujo-de-trabajo-con-ambientes)
- [Conclusiones](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#conclusiones)

En el desarrollo de proyectos científicos y de ciencia de datos, la gestión de dependencias es uno de los mayores retos. Trabajar en **local** (con herramientas como Anaconda o PyCharm) ofrece estabilidad y persistencia, mientras que trabajar en la **nube** (como Google Colab) prioriza la inmediatez y el uso de recursos externos. Este post se centra en dominar la terminal de Anaconda para un flujo de trabajo eficiente.

## 1\. Conceptos Fundamentales: Conda vs. Anaconda[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#1-conceptos-fundamentales-conda-vs-anaconda)

Es común confundir estos términos, pero entender su diferencia es clave para saber qué instalar:

- **Conda:** Es el motor. Un sistema de gestión de paquetes y entornos de código abierto que instala, ejecuta y actualiza dependencias rápidamente.
- **Anaconda:** Es la “suite” completa. Una distribución que incluye Python, R y cientos de paquetes científicos preinstalados.
- **Miniconda:** Una versión minimalista que solo incluye Conda y sus dependencias básicas. Ideal si prefieres instalar solo lo que necesitas.

## 2\. Gestión de Paquetes (Packages)[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#2-gesti%C3%B3n-de-paquetes-packages)

Para instalar paquetes en Python, se recomienda usar **Conda** en lugar de PIP cuando se trabaja en este ecosistema, ya que Conda garantiza la compatibilidad binaria de las librerías en sus propios repositorios.

### Comandos Esenciales de Paquetes[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#comandos-esenciales-de-paquetes)

| Acción | Comando |
| --- | --- |
| **Listar instalados** | `conda list` |
| **Buscar paquete** | `conda search NOMBRE` |
| **Instalar último** | `conda install NOMBRE` |
| **Instalar versión** | `conda install NOMBRE=1.4.2` |
| **Actualizar** | `conda update NOMBRE` |
| **Eliminar** | `conda remove NOMBRE` |

> **Nota sobre Versionamiento:** Conda utiliza el sistema **MAJOR.MINOR.PATCH**. Un cambio en _Major_ implica cambios drásticos, _Minor_ añade funciones y _Patch_ corrige errores sin afectar la compatibilidad.

## 3\. Canales (Channels)[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#3-canales-channels)

Los canales son las direcciones o repositorios de donde se descargan los paquetes. El canal por defecto es el de Anaconda, pero existen alternativas comunitarias muy potentes como `conda-forge`.

- **Buscar en un canal específico:** `conda search -c conda-forge NOMBRE`
- **Instalar desde un canal:** `conda install -c conda-forge NOMBRE`

## 4\. Gestión de Ambientes (Environments)[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#4-gesti%C3%B3n-de-ambientes-environments)

Los ambientes permiten aislar proyectos. Por ejemplo, puedes tener un ambiente con Python 3.7 para una tesis y otro con Python 3.10 para pruebas, sin que choquen entre sí.

### Flujo de trabajo con Ambientes[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#flujo-de-trabajo-con-ambientes)

1. **Listar todos los ambientes:** `conda env list` (El asterisco `*` indica el ambiente activo).
2. **Crear un ambiente nuevo:** `conda create -n mi_proyecto python=3.9`.
3. **Activar / Desactivar:**
 - Activar: `conda activate mi_proyecto`
 - Salir: `conda deactivate`
4. **Eliminar un ambiente:** `conda env remove -n mi_proyecto`.

## Conclusiones[#](https://vilcagamarracf.github.io/posts/manejo_paquetes_anaconda/#conclusiones)

La elección entre trabajar en la nube o en local depende de tus necesidades de hardware y persistencia de datos. Mientras que **Colab** es excelente para prototipado rápido, el manejo de ambientes en **local** con Anaconda te otorga el control total sobre las versiones y la reproducibilidad de tus investigaciones científicas.

---

_Muchas gracias por leer. ¡Saludos!_ 🚀