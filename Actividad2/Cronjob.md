Actividad 2

CRONJOB

Escritorio/Sopes1/Tareas/so1_actividades_202004060/Actividad2/script.sh

Esta línea define la programación del cronjob. Cada campo separado por espacios representa una parte de la programación, y juntos forman una expresión cron que determina cuándo y con qué frecuencia se ejecutará el script.

    El primer campo */5 indica el valor para los minutos. En este caso, */5 significa "cada 5 minutos". Es decir, el cronjob se ejecutará cuando los minutos sean múltiplos de 5 (0, 5, 10, 15, 20, etc.).

    El segundo campo * indica el valor para las horas. En este caso, el asterisco * significa "cualquier hora", lo que indica que el cronjob puede ejecutarse en cualquier hora.

    El tercer campo * indica el día del mes. Aquí también, el asterisco * significa "cualquier día del mes", lo que indica que el cronjob puede ejecutarse cualquier día del mes.

    El cuarto campo * indica el valor para el mes. Igual que antes, el asterisco * significa "cualquier mes", lo que indica que el cronjob puede ejecutarse en cualquier mes.

    El quinto campo * indica el día de la semana. Nuevamente, el asterisco * significa "cualquier día de la semana", lo que indica que el cronjob puede ejecutarse cualquier día de la semana.

Finalmente, el comando /Escritorio/Sopes1/Tareas/so1_actividades_202004060/Actividad2/script.sh indica la ruta absoluta del script que se ejecutará cuando el cronjob se active cada 5 minutos.

En resumen, esta configuración de cronjob ejecutará el script script.sh ubicado en la ruta especificada cada 5 minutos, sin importar la hora, día del mes, mes o día de la semana.

