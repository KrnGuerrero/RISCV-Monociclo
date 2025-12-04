# Monociclo DE1-SoC Project

Este proyecto implementa un monociclo utilizando un FPGA DE1-SoC. El diseño permite realizar operaciones aritméticas básicas (suma, resta, AND, OR) utilizando interruptores para ingresar dos números y seleccionar la operación deseada.

## Estructura del Proyecto

El proyecto está organizado en las siguientes carpetas:

- **hardware/**: Contiene el diseño del FPGA y los archivos de prueba.
  - **fpga/**: Archivos fuente del diseño del FPGA.
    - **src/**: Código fuente en SystemVerilog.
    - **constraints/**: Asignaciones de pines para el FPGA.
    - **quartus/**: Archivo del proyecto de Quartus.
  - **tb/**: Testbenches para verificar el funcionamiento del diseño.
  
- **software/**: Contiene el software para el HPS (Hard Processor System).
  - **hps/**: Código fuente y Makefile para el software del HPS.
  - **baremetal/**: Entorno de software bare-metal.
  
- **docs/**: Documentación del proyecto.
  - **spec.md**: Especificaciones del diseño.
  - **interface.md**: Descripción de las interfaces entre componentes.
  
- **scripts/**: Scripts para automatizar tareas.
  - **program_fpga.sh**: Programa el FPGA con el diseño compilado.
  - **build_hps.sh**: Automatiza el proceso de construcción del software HPS.
  
- **tests/**: Pruebas para el diseño del FPGA.
  - **sim/**: Scripts para ejecutar simulaciones.

## Instrucciones de Configuración

1. **Configuración del Entorno**: Asegúrate de tener instalado Quartus y las herramientas necesarias para compilar el diseño del FPGA.
2. **Compilación del FPGA**: Navega a la carpeta `hardware/fpga/quartus` y abre el archivo `project.qpf` en Quartus. Compila el diseño.
3. **Programación del FPGA**: Ejecuta el script `scripts/program_fpga.sh` para programar el FPGA con el diseño compilado.
4. **Compilación del Software HPS**: Navega a `software/hps` y ejecuta `make` para compilar el software del HPS.
5. **Ejecución de Pruebas**: Utiliza el script `tests/sim/run_sim.sh` para ejecutar las pruebas de simulación.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para discutir cambios o mejoras.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.