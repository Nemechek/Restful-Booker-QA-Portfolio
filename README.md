#  API Quality Assurance Portfolio Project

Proyecto de testing funcional y automatización de API realizado sobre la plataforma pública **Restful-Booker**. Este proyecto demuestra habilidades de análisis de calidad, diseño de casos de prueba avanzados, validación mediante Postman y reporte de incidencias.

---

##  1. Objetivo del Testing
Evaluar la estabilidad, la integridad de los datos y el manejo de excepciones de la API. El enfoque principal consistió en validar el comportamiento del sistema ante entradas correctas (casos positivos) y entradas con datos erróneos o inválidos (casos negativos), aplicando técnicas de ingeniería de QA.

---

##  2. Alcance (Scope)
* **Módulo Auth (`/auth`):** Generación y validación de tokens de acceso.
* **Módulo Booking (`/booking`):** Operaciones de creación de reservas y validación de restricciones de esquemas de datos.
* **Fuera de alcance:** Pruebas de rendimiento (stress/load testing) y seguridad avanzada (SQL Injection).

---

##  3. Técnicas de Testing Aplicadas
* **Clases de Equivalencia:** División de los datos de entrada en conjuntos válidos e inválidos (ej. validación de tipos de datos en campos numéricos y booleanos).
* **Análisis de Valores Límite (BVA):** Verificación de restricciones temporales en las fechas de estadía (`checkin` y `checkout`).
* **Pruebas Automatizadas en Postman:** Scripts en JavaScript integrados para la validación automática de códigos de estado HTTP y propiedades de las respuestas JSON.

---

##  4. Estructura del Repositorio

api-testing-portfolio/
│
├── README.md                              # Documentación del proyecto
├── postman/


│   ├── Restful-Booker.postman_collection.json  # Colección con tests automatizados
│   └── Restful-Booker.postman_environment.json # Variables de entorno
└── reports/
    └── bug_report.md                      # Reporte detallado de hallazgos


## 5. Conclusiones y Hallazgos
La API demuestra un comportamiento estable para flujos estándar (casos positivos). Sin embargo, se identificaron áreas de oportunidad críticas en la validación de esquemas de datos del lado del servidor (como se detalla en el Reporte de Bugs), lo cual demuestra la importancia de contar con una capa robusta de validación de entradas para prevenir la persistencia de datos corruptos.
