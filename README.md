## **1. ¿Qué es Erlang?**

Erlang es un **lenguaje de programación funcional** creado en 1986 por **Ericsson** (una empresa de telecomunicaciones sueca).

Fue diseñado específicamente para:

- **Concurrencia masiva** → manejar miles o millones de procesos al mismo tiempo.
- **Sistemas distribuidos** → que corren en varios servidores y trabajan juntos.
- **Alta disponibilidad** → que no se caigan, o que se recuperen solos en segundos.

Por eso, Erlang se usa mucho en telecomunicaciones, sistemas financieros y aplicaciones donde la **comunicación rápida y confiable** es vital (WhatsApp, por ejemplo, está hecho en gran parte sobre Erlang).

---

## **2. Palabras y conceptos importantes**

Voy a explicarte cada término sin asumir que ya lo conoces:

### **BEAM**

- Es la **máquina virtual** en la que corren Erlang y Elixir (como la JVM en Java).
- Administra los **procesos ligeros**, la memoria y la comunicación entre ellos.

### **Proceso ligero**

- En Erlang/Elixir, un “proceso” no es un proceso del sistema operativo ni un thread pesado.
- Es una unidad de ejecución extremadamente liviana que maneja la BEAM.
- Ventaja: puedes tener cientos de miles sin saturar el sistema.

### **Modelo de actores**

- Es una forma de organizar programas concurrentes.
- Cada proceso es un “actor”: tiene su propio estado y se comunica solo enviando y recibiendo mensajes.
- No hay memoria compartida, así que no necesitas bloqueos (`synchronized`, `locks`).

### **OTP (Open Telecom Platform)**

- Un conjunto de librerías y herramientas que vienen con Erlang para construir sistemas robustos.
- Incluye:
    - **Supervisores**: procesos que vigilan a otros y los reinician si fallan.
    - **GenServer**: una estructura para procesos que manejan mensajes de manera estándar.
    - **Aplicaciones distribuidas**: para correr tu programa en varios nodos conectados.

### **Let it crash**

- Filosofía de Erlang: no intentes evitar todos los errores; deja que el proceso falle y deja que un **supervisor** lo reinicie limpio.
- Esto evita que un error escondido destruya todo el sistema.
