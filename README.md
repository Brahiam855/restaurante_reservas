## Justificación
El sistema de reservas de restaurante se ha diseñado utilizando una **arquitectura en capas**, que permite separar claramente las responsabilidades de cada módulo y facilitar su mantenimiento, escalabilidad y testabilidad. Esta estructura asegura que cada componente tenga un propósito específico, cumpliendo el **Principio de Responsabilidad Única (SRP)**.  

- **Capa de Presentación:** Se encarga de la interacción con el cliente, mostrando formularios de reserva, calendarios de disponibilidad, confirmaciones y el historial de reservas. Su independencia garantiza que cambios en la interfaz no afecten la lógica de negocio ni la base de datos.  
- **Capa de Lógica de Negocio:** Incluye los gestores de Reservas, Disponibilidad, Usuarios y Notificaciones. Cada gestor maneja funciones específicas, evitando que los cambios en uno afecten al resto del sistema. Esto facilita pruebas unitarias aisladas y permite optimizar cada módulo de forma independiente.  
- **Capa de Datos:** Centraliza toda la información en tablas estructuradas para Usuarios, Reservas, Mesas y Horarios, asegurando integridad, consistencia y rápida recuperación de datos. Su diseño modular permite escalabilidad y facilita la conexión con otras capas y servicios externos.  
- **Servicios Externos:** Incluye APIs de correo, SMS, pagos y mapas, integradas de manera independiente para que las actualizaciones externas no afecten la lógica interna del sistema.  

Esta arquitectura mejora la **robustez** del sistema, minimizando errores y conflictos entre módulos, y permite que el sistema sea **flexible**, fácil de mantener y expandir. Además, la separación de capas ayuda a que el desarrollo sea más organizado, reduce la complejidad, y proporciona una experiencia eficiente y confiable tanto para los clientes como para los administradores del restaurante.  

En conjunto, la implementación de estas capas y la aplicación de SRP aseguran un sistema bien estructurado, profesional y preparado para escalar según las necesidades futuras, cumpliendo con estándares de calidad de software y buenas prácticas de ingeniería.
