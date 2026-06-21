# ISAM SYSTEM

Sistema de escritorio para la captura, emision, anulacion e historial de recibos ISAM.

Este repositorio contiene el primer prototipo funcional del sistema, desarrollado como alternativa a un flujo anterior basado en Excel/VBA. La aplicacion esta pensada para ejecutarse en Windows sin depender de Excel ni macros.

## Estado del proyecto

Prototipo funcional inicial.

Incluye:

- Captura de recibos.
- Serie y numero de recibo.
- Numeracion automatica del siguiente recibo despues del primer registro.
- Distrito, canton y comunidad mediante listas desplegables.
- Detalle de conceptos con codigo, descripcion y monto.
- Calculo automatico del total.
- Conversion del total a letras.
- Generacion de PDF.
- Apertura automatica del PDF generado.
- Anulacion de recibos con motivo.
- Historial local de recibos.
- Base de datos SQLite local.

## Tecnologias utilizadas

- C#
- .NET 8
- Windows Forms
- SQLite
- QuestPDF
- Git LFS para almacenar el ejecutable grande

## Ejecutable

El prototipo portable se encuentra en:

```text
ISAM_Prototipo/ISAM.exe
```

Para ejecutarlo, abrir `ISAM.exe` en Windows.

La primera vez que se ejecute, el sistema creara automaticamente carpetas locales para datos y PDFs junto al ejecutable.

## Estructura esperada de uso

```text
ISAM_Prototipo/
  ISAM.exe
  LatoFont/
  data/
    isam.db
  pdf/
    emitidos/
    anulados/
```

Las carpetas `data` y `pdf` pueden crearse automaticamente al ejecutar el sistema.

## Migracion entre equipos

Para mover el sistema a otro equipo Windows, copiar completa la carpeta:

```text
ISAM_Prototipo
```

No copiar solamente el archivo `ISAM.exe`, porque el generador de PDF puede requerir archivos de soporte incluidos en la carpeta.

## Notas sobre Git LFS

El ejecutable supera el limite normal de 100 MB de GitHub, por eso se administra mediante Git LFS.

Antes de clonar o trabajar con el repositorio en otra computadora, instalar Git LFS y ejecutar:

```bash
git lfs install
git lfs pull
```

## Licencia

Este proyecto usa una licencia privada de uso interno. Ver el archivo:

```text
LICENSE
```

El uso, copia, modificacion y distribucion esta permitido unicamente al personal autorizado.

## Autor
Alexander Vásquez
Cristobal Torres

