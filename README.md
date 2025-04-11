# examen_ud6_ed
***examen realizado por Javier López Gutiérrez***
---

### Crear contenedor Sonar Qube

```
docker
docker run -d --name sonarqube_examen -p 9009:9000 sonarqube:latest
docker ps
```
Abrir en el navegador: http://localhost:9009
### Creación de proyecto local en Sonar Qube

Generación de Token
sqp_14944e6b17e1ff07a68de3c700be857994165910

---

## 2. Ejercicio 1: Refactorización (7 puntos) 

```
sonar.projectKey=ed_ex6_refactorizacion
sonar.host.url=http://localhost:9009
sonar.token=sqp_14944e6b17e1ff07a68de3c700be857994165910
sonar.language=java
sonar.sources=src
sonar.java.binaries=target/classes
```
for /r src %f in (*.java) do javac -d target\classes "%f"

--- 

### PROBLEMAS A LA HORA DE REALIZAR LA PRACTICA
No puedo Ejecutar el proyecto de manera local de SonarQube Server me aparecen los siguientes errores y no se solucionarlo por lo que no puedo demostrar que sepa refactorizar.
el error en cmd es el siguiente
```bash
C:\Users\JAVI\eclipse-workspace-entornos\ed_ex6_refactorizacion>sonar-scanner
09:28:56.422 INFO  Scanner configuration file: C:\sonar-scanner-7.0.2.4839-windows-x64\bin\..\conf\sonar-scanner.properties
09:28:56.432 INFO  Project root configuration file: NONE
09:28:56.470 INFO  SonarScanner CLI 7.0.2.4839
09:28:56.475 INFO  Java 17.0.13 Eclipse Adoptium (64-bit)
09:28:56.477 INFO  Windows 10 10.0 amd64
09:28:56.525 INFO  User cache: C:\Users\JAVI\.sonar\cache
09:28:57.702 INFO  JRE provisioning: os[windows], arch[amd64]
09:28:58.265 ERROR Failed to query JRE metadata: . Please check the property sonar.token or the environment variable SONAR_TOKEN.
09:28:58.266 INFO  EXECUTION FAILURE
09:28:58.272 INFO  Total time: 1.856s
```

*el error aparece en que la propiedad de sonar.token da error pero se encuentra correctamente configurada en `sonar-project.properties`*

<img src="images/Captura de Pantalla cmd.png" width="300"/>

| columna | columna 2 | columna 3 |
|---------|-----------|-----------|
| ejemplo | ejemplo   | ejemplo   |
| ejemplo | ejemplo   | ejemplo   |
| ejemplo | ejemplo   | ejemplo   |