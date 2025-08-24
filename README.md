# 🚀 Recargi: Pagos de Suscripciones Streaming Sin Tarjeta Internacional 🚀

**Estado:** En Producción (Rentable y Operativa)
**Tecnologías Clave:** Kotlin (Jetpack Compose), Node.js (Express.js, Puppeteer), AWS (EC2, RDS, S3), MySQL, Cloudflared, Firebase Cloud Messaging.

## 🌟 Visión General del Proyecto

Recargi es una innovadora y rentable aplicación móvil diseñada para solventar la problemática de realizar pagos de suscripciones a servicios de streaming en Venezuela, un mercado con acceso limitado a métodos de pago internacional. Permite a los usuarios recargar saldo en moneda local (Bolívares) y gestionar sus pagos de streaming de forma automática y sencilla.

Este proyecto representa una solución full-stack completa, desde la conceptualización de una idea de negocio hasta el despliegue, automatización avanzada y monetización exitosa en un entorno de mercado desafiante. Subraya mi capacidad para diseñar arquitecturas resilientes, desarrollar componentes de software complejos y asegurar la operativa continua de un producto en producción.

## 📈 Impacto y Logros Cuantificables

* **Rentabilidad Comprobada:** Generó **+$10,000 en ganancias netas** y un **flujo total de +$40,000 en ventas** en el mercado venezolano durante su primer año de operación.
* **Operación Autónoma y Escalable:** Establecí una infraestructura y lógica de negocio que permite una operación altamente automatizada para la venta y entrega de gift cards, demostrando la robustez y escalabilidad de la solución en condiciones de mercado únicas.
* **Adopción por Usuarios:** [Número de instalaciones/usuarios activos] en Google Play Store con una calificación promedio de [X.X] estrellas.
* **Solución a una Necesidad Real:** Proporcionó una solución crítica y confiable a un problema masivo de acceso a servicios digitales en un mercado con fuertes restricciones económicas.

## 📸 Imágenes y Media

Aquí puedes ver la aplicación Recargi en acción, junto con vistas de su panel de administración y algunas de sus características clave.

### Aplicación Móvil (Frontend)

<img src="https://github.com/user-attachments/assets/8b07a525-fc1d-4185-9975-762df60d9c53" alt="Captura de pantalla de la app Recargi" width="200" />

_Captura de pantalla: Interfaz principal de Recargi._

<!-- Reproductor incrustado de Vimeo (más fiable para GitHub) -->
  <iframe src="https://player.vimeo.com/video/1112723695?badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479"
          width="700" height="394" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share" referrerpolicy="strict-origin-when-cross-origin"
          style="display:block; margin:20px auto; border-radius: 8px;">
  </iframe>

_Captura de pantalla: Pantalla de añadir saldo, destacando la animación sutil en el botón._

<img src="https://github.com/user-attachments/assets/69ea8b40-30c7-4f9f-8aae-0665d7879e24" alt="Captura de pantalla de la app Recargi" width="200" />

_Captura de pantalla: Avisos inteligentes._

### Panel de Administración Web


_Captura de pantalla: Dashboard de Analytics en el panel de administración, mostrando ganancias y métricas._


_Captura de pantalla: Sección de gestión de depósitos, con opciones de verificación manual._


_Captura de pantalla: Vista del stock de Gift Cards y gestión de órdenes pendientes._

### Demostración (Opcional - GIF/Video Corto)


_GIF/Video: Demostración rápida del proceso de recarga de saldo o compra de una gift card._

---

## ✨ Características Principales

* **Aplicación Móvil Intuitiva (Kotlin / Jetpack Compose):**
    * Interfaz de usuario moderna y fluida, desarrollada con Material UI 3 y principios de diseño centrados en el usuario.
    * Animaciones suaves y originales para una experiencia de usuario excepcional y atractiva.
    * Animaciones estratégicas y sutiles en botones clave (e.g., "+ Añadir Saldo") diseñadas para optimizar la interacción y conversión del usuario.
    * Gestión sencilla de suscripciones, recargas de saldo y monitoreo del estado de la billetera del usuario.
* **Panel de Administración Web (para Operadores):**
    * Interfaz intuitiva para el control total de la operación de Recargi.
    * **Analytics avanzados:** Visualización en tiempo real de ganancias mensuales, depósitos totales recibidos, flujo de caja actual en la app (saldo acumulado de clientes), y métricas de registro de usuarios (diario, mensual, anual). Todo se actualiza automáticamente según ajustes de precios, ganancias y costos de productos.
    * **Gestión de Depósitos:** Panel para la verificación manual de pagos pendientes (en caso de fallos del scrapper) y corrección de depósitos denegados erróneamente.
    * **Órdenes y Stock:** Gestión completa de órdenes de compra (entregadas, rechazadas, pendientes), con notificaciones automáticas para pedidos pendientes.
    * Control de stock de Gift Cards, permitiendo la carga anticipada para entrega inmediata.
    * **Exchange (Tasa de Cambio):** Herramienta para actualizar dinámicamente la tasa de cambio de Bolívares a Dólares en la aplicación.
* **Automatización Crítica:**
    * Sistema de stock automático de Gift Cards para entrega inmediata al cliente.
    * Verificación automática de depósitos bancarios de clientes, logrando tiempos de confirmación inferiores a 10 segundos.

## 🛠️ Stack Tecnológico

* **Frontend Móvil:** Kotlin, Jetpack Compose, Android Studio, Material UI 3
* **Backend:** Node.js, Express.js, JavaScript
* **Bases de Datos:** MySQL (gestionado vía Amazon RDS)
* **Cloud / Infraestructura:** Amazon Web Services (AWS) - EC2, RDS, S3, [Otros servicios AWS usados, ej. CloudWatch para monitoreo, IAM para gestión de acceso, SNS para notificaciones internas].
* **Automatización:** Node.js (con Puppeteer para scrapping), Cloudflared (para túnel seguro).
* **Mensajería / Notificaciones:** Firebase Cloud Messaging (FCM).
* **Herramientas:** VS Code, Git.

## ⚙️ Componentes Clave y Funcionamiento Detallado

La arquitectura de Recargi está diseñada para ser eficiente, segura y altamente automatizada, dividida en varios componentes que interactúan de forma fluida:

### 1. 🤖 El Scrapper (Local - Node.js con Puppeteer)

* **Función:** Automatiza la extracción de movimientos bancarios para la verificación de depósitos.
* **Tecnología:** Desarrollado en **Node.js** utilizando **Puppeteer** para simular la interacción humana con la interfaz web del banco.
* **Seguridad de Credenciales:** Las credenciales bancarias residen **exclusivamente en mi máquina local**, nunca salen a la nube o al servidor, garantizando la máxima seguridad.
* **Tácticas Anti-Detección:** Implementa técnicas avanzadas para evitar que los sistemas de seguridad del banco detecten la presencia del scrapper, asegurando una operación continua.
* **Túnel Seguro (Cloudflared):** Un túnel de **Cloudflared** expone un endpoint seguro desde mi máquina local al servidor en AWS.
* **Mecanismo de Verificación:**
    * Al iniciarse, el scrapper registra su disponibilidad en el servidor de AWS como un "dispositivo de verificación".
    * Cuando un cliente realiza un depósito y lo registra en la app (proporcionando los últimos 6 dígitos de la referencia, un método común en Venezuela), el servidor invoca el endpoint seguro del túnel en mi máquina local.
    * El scrapper extrae los movimientos bancarios recientes, los **formatea en JSON** y los **normaliza** para una consistencia de datos.
    * Esta información es enviada de vuelta al servidor de AWS, que compara los movimientos con los depósitos pendientes.
* **Velocidad Record:** Este sistema permite la verificación de depósitos de clientes en **menos de 10 segundos**, automatizando un proceso que tradicionalmente se realiza manualmente en Venezuela.

### 2. 📊 El Panel de Administración (Web)

* **Función:** Interfaz web completa para la gestión y monitoreo integral de la aplicación.
* **Analytics Detallados:**
    * Visualización de ganancias mensuales generadas por la aplicación.
    * Conteo de depósitos totales y el dinero total depositado en las billeteras de los clientes.
    * Métricas de registro de usuarios (diario, mensual, anual).
    * Todos los analytics se actualizan de forma **automática y dinámica**, basándose en los ajustes de precios, ganancias y costos de los productos configurados en el servidor, eliminando la necesidad de cálculos manuales.
* **Gestión de Depósitos:** Permite la verificación manual de pagos pendientes (cuando el scrapper no puede operar) y la corrección de errores (ej. depósitos denegados por montos incorrectos).
* **Órdenes Pendientes y Stock:**
    * Muestra todas las órdenes de compra realizadas por los usuarios (entregadas, rechazadas, pendientes).
    * Si una gift card está en stock, se entrega automáticamente al cliente.
    * En caso de que no haya stock, se genera una orden pendiente y se envía una notificación push a los administradores para su resolución y reposición de stock.
* **Exchange (Tasa de Cambio):** Herramienta esencial para actualizar la tasa de cambio de Bolívares a Dólares utilizada en la aplicación.

### 3. 🧠 El Servidor (AWS - Node.js)

* **Función:** El cerebro de toda la aplicación, orquestando todas las operaciones.
* **Gestión Centralizada:** Mantiene sesiones de usuario (con caducidad), gestiona todas las llamadas de la aplicación móvil y del panel de administración.
* **Notificaciones (Firebase Cloud Messaging):** Envía notificaciones push a los dispositivos (clientes y administradores) en tiempo real para eventos clave: entrega de pedidos, verificación de depósitos, incidencias o notificaciones generales.
* **Base de Datos:** Almacena toda la información relevante de forma segura en MySQL (Amazon RDS).
* **Seguridad:** Implementa límites de llamadas a la API para prevenir ataques (rate limiting) y otras medidas de seguridad.
* **Optimización:** Desarrollado con prácticas para evitar fugas de memoria y optimizado al máximo para funcionar de manera eficiente en entornos de bajos recursos.

### 4. 📱 La Admin App (Aplicación de Notificaciones para Administradores)

* **Función:** Una aplicación ligera y sin interfaz diseñada exclusivamente para que los teléfonos de los administradores reciban notificaciones críticas del servidor.
* **Tipos de Notificaciones:** Informa sobre la entrega exitosa de gift cards, nuevas órdenes pendientes, el registro y renovación de cuentas, el registro, verificación o denegación de depósitos, y otros eventos operacionales importantes.

## ⚙️ Arquitectura de la Solución (Conceptual y Detallada)

<img width="4950" height="3465" alt="Diagrama Recargi" src="https://github.com/user-attachments/assets/d144b753-34f7-48a8-adfb-b5e6a039ce1d" />

_Diagrama conceptual detallado de la arquitectura de Recargi_

**Descripción del Flujo General:**
El usuario interactúa con la **App Móvil**, que se comunica con el **Servidor API** en AWS. El servidor, el núcleo, gestiona la lógica, interactúa con **RDS (MySQL)** y **S3**. Para la verificación de depósitos, el servidor se comunica con el **Scrapper local** (vía **Cloudflared**), que a su vez interactúa con el banco. Los administradores gestionan la plataforma a través del **Panel de Administración Web** y reciben alertas en tiempo real en la **Admin App** (vía Firebase).

## 🧩 Desafíos Técnicos y Soluciones Innovadoras

1.  **Verificación Bancaria Segura y Ultra-rápida:**
    * **Desafío:** Automatizar la verificación de depósitos en un sistema bancario local (Venezuela) que no ofrece APIs públicas, mientras se protegen las credenciales bancarias y se evita la detección de bots. El objetivo era superar los métodos manuales existentes.
    * **Solución:** Desarrollo de un **scrapper de Node.js con Puppeteer** ejecutándose en un entorno local seguro. La comunicación con el servidor de AWS se realiza mediante un **túnel de Cloudflared** con un endpoint seguro, garantizando que las credenciales bancarias nunca salgan del entorno local. Este sistema verifica los depósitos en **menos de 10 segundos**, una mejora sustancial sobre los procesos manuales.
2.  **Optimización Extrema de Costos y Recursos en AWS:**
    * **Desafío:** Mantener una operación rentable y una infraestructura eficiente en AWS, maximizando el rendimiento con recursos mínimos, especialmente crucial en un contexto económico desafiante.
    * **Solución:** Diseño de un servidor Node.js optimizado para baja huella de memoria, dimensionamiento preciso de instancias EC2 y RDS, uso estratégico de S3 para almacenamiento de costos reducidos, y monitoreo constante para identificar y eliminar gastos innecesarios.
3.  **Desarrollo Full-Stack Autónomo y Mantenimiento Continuo:**
    * **Desafío:** Gestionar y mantener una aplicación móvil, un backend complejo, un panel de administración, un scrapper y una app de notificaciones como un único desarrollador, asegurando la escalabilidad y la fiabilidad.
    * **Solución:** Adopción de un diseño modular, uso intensivo de automatización para tareas repetitivas (stock, verificaciones), implementación de Firebase para notificaciones en tiempo real, y un enfoque proactivo en el monitoreo y la resolución de problemas.
4.  **Adaptación a un Mercado con Restricciones:**
    * **Desafío:** Crear una solución de pagos digitales en un mercado con barreras significativas para transacciones internacionales y una moneda volátil.
    * **Solución:** Desarrollo de un sistema de recarga en moneda local, gestión dinámica de la tasa de cambio y una operación autónoma de suministro de productos digitales para superar las limitaciones del mercado.

## 🤝 Contacto

Para más detalles sobre este proyecto o mi trabajo, no dudes en contactarme en [hernandez.rafael.0309@gmail.com](mailto:hernandez.rafael.0309@gmail.com) o visitar mi [Portafolio Online](https://raalplay.github.io/portfolio).
