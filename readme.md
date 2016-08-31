Prueba de concepto para el curso Advanced Process Development with Red Hat JBoss BPM Suite
Author: Crystian Anaya Franco
=======================
Correo: canaya@redhat.com
=======================

El presente repositorio contiene el proyecto de prueba de concepto para el curso Advanced Process Development with Red Hat JBoss BPM Suite de acuerdo a las instrucciones de la signación final. Dicho proyecto puede ser importdo en la consola de Red Hat BPM 6.3, así mismo puede ser depployado y ejecutado en kie-server de Red Hat Jboss BPM SUITE 6.3

Para los fines anteriores se detallan lo siguiente:
El usuario habilitado para seguir el flujo del proceso es jboss.
El flujo del proceso de negocio esta dictado por el archivo TestProcess.bpmn2, que hace alución a lo que representaría el new order permitting business process de las instrucciones en la asignación final. A partir de este será poible iniciar el flujo.

Descripción basica del flujo:
El flujo inicia por una a tarea de usuario para crear la solicitud de un panel solar. Debido a que el negocio esta definido por una asociación de propietarios el owner de esta debe revisar la solicitud y aceptarla (tarea de usuario aceptar solicitud) o rechazarla, en caso de rechazo, será elevada a un ejecutivo (tarea de usuario rechazar solicitud). Concluido esto, se pasará a la tarea de habilitar permisos, referidos a permisos de gobierno en los requerimientos. Al pasar este estado, se encontrarán las tareas de usuario paralelas, Aprobar permiso elec y Aprobar perimso Estr. A través de estas tareas de suario en paralelo se podrán aprobar los permisos de gobierno necesarios. Una tarea de script se encarga de actualizar los datos del proceso de negocio llevado hasta ahora, para en el ultimo estado mostrar dichos resulados y conocer si fue o no aprobada la solicitud antes de finalizar el proceso.
