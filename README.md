# CUA Interaction Test Environment

[![Website Status](https://img.shields.io/website?url=https%3A%2F%2Flolamaturana.github.io%2Fcafe.maturana%2F)](https://lolamaturana.github.io/cafe.maturana/)

Este repositorio contiene el código fuente de una página web estática diseñada específicamente como **entorno de pruebas y validación** para el desarrollo de un Computer Using Agent (CUA).

Puedes visitar la página de pruebas en vivo aquí: **[CUA Test Page](https://lolamaturana.github.io/cafe.maturana/)**


## Propósito del Proyecto

El desarrollo de agentes autónomos basados en Modelos de Lenguaje Grandes (LLM) requiere entornos controlados para evaluar su comportamiento. Esta página web fue creada para:

1. **Crear escenarios atómicos:** Permitir la depuración sistemática del agente aislando diferentes tipos de interacciones web.
2. **Validar el Model Context Protocol (MCP):** Probar la capacidad del agente para leer e interactuar con el DOM utilizando el **árbol de accesibilidad** (a través de herramientas como Playwright), evaluando su eficacia sin depender de modelos de visión.
3. **Optimización de Prompts:** Servir como un campo de pruebas determinista para iterar y mejorar las instrucciones (*prompts*) dadas al LLM.

## Elementos de Interacción (Features)

La página incluye una variedad intencionada de componentes web estándar y complejos para desafiar y evaluar al agente, tales como:

* **Campos de entrada de texto:** Inputs simples, textareas y campos con validación.
* **Selectores y Menús:** Dropdowns, checkboxes y radio buttons.
* **Botones y Formularios:** Botones de envío, botones de acción y formularios completos para simular flujos de usuario.


## Cómo funciona en el contexto del CUA

A diferencia de los enfoques basados en capturas de pantalla, esta página está optimizada para que un agente analice su **estructura semántica**. El CUA accede a esta URL, extrae una instantánea del árbol de accesibilidad mediante MCP, y el LLM decide qué acciones tomar (ej. `click()`, `fill()`, `selectOption()`) basándose puramente en texto y jerarquía HTML. Esto garantiza una interacción más ligera, rápida y determinista.


## Autora

Desarrollado como parte de la investigación e implementación de sistemas CUA durante mi etapa en BBVA AI Factory.
