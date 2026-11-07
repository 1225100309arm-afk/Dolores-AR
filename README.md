#  Rally de la Independencia AR — Dolores Hidalgo

Juego de **realidad aumentada por ubicación** hecho en Flutter con **TDD** (Desarrollo Guiado por Pruebas).
El jugador recorre Dolores Hidalgo buscando a 6 personajes de la Independencia con un **radar**, un indicador de **"frío o caliente"** y la **cámara**. Al acercarse a 15 m o menos, responde una **pregunta de historia** para atraparlo y guardarlo en su **álbum**.



##  Cómo ejecutarlo

```bash
flutter pub get
flutter test        # deben pasar todas las pruebas
flutter run         # con el emulador abierto
```



##  Evidencias

### Código

**C1 · Paquetes del proyecto (`pubspec.yaml`)**
![C1](capturas/C1_pubspec.png)

**C2 · Permisos de Android (`AndroidManifest.xml`)**
![C2](capturas/C2_permisos.png)

**C3 · Función `destino` (Ronda 2)** — si camino X metros con rumbo R, ¿a dónde llego?
![C3](capturas/C3_destino.png)

**C4 · Azar con raíz cuadrada (Ronda 4)** — el `Random` se recibe como parámetro para poder probarlo con semilla.
![C4](capturas/C4_aparicion.png)

**C5 · Radar y frío o caliente (Ronda 5)**
![C5](capturas/C5_radar.png)

**C6 · Motor de realidad aumentada (Ronda 6)**
![C6](capturas/C6_motor_ar.png)

**C7 · Sealed class de resultados (Ronda 7)**
![C7](capturas/C7_sealed.png)

**C8 · Reglas de captura (Ronda 7)** — 15 m, 100/50 puntos, huida tras 2 fallos.
![C8](capturas/C8_capturar.png)

**C9 · Contrato de almacenamiento (Ronda 8)** — solo se guardan ids y puntaje, nunca coordenadas.
![C9](capturas/C9_almacen.png)

**C10 · Caminar en modo demo (Ronda 9)** — reutiliza `destino()`.
![C10](capturas/C10_demo.png)

**C11 · ViewModel `capturar()` (Ronda 10)**
![C11](capturas/C11_viewmodel.png)

**C12 · Radar con CustomPainter (Ronda 11)**
![C12](capturas/C12_custompainter.png)

**C13 · Switch exhaustivo (Ronda 11)**
![C13](capturas/C13_switch.png)

### Pruebas

**P1 · Prueba "ida y vuelta" de `destino` en 9 direcciones**
![P1](capturas/P1_test_geo.png)

**P2 · Prueba de reglas: con 2 fallos el personaje se escapa**
![P2](capturas/P2_test_partida.png)

**P3 · Azar reproducible: misma semilla = mismo resultado**
![P3](capturas/P3_test_aparicion.png)

### App en el emulador

![E4](capturas/E4_album.png)

![E1](capturas/E1_inicio.png)


![E2](capturas/E2_demo_radar.png)







---

