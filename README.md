# examen_ud6_ed
***examen realizado por Javier López Gutiérrez***
---

### Crear contenedor Sonar Qube

```
docker
docker run -d --name sonarqube_examen -p 9009:9000 sonarqube:latest
docker ps
```

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