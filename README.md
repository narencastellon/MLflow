Elaborado por: **Naren Castellon**
# MLflow
Introducción a MLflow  MLflow es una plataforma de código abierto para el ciclo de vida del aprendizaje automático (ML), con un enfoque en la reproducibilidad, el entrenamiento y la implementación. Está basado en un diseño de interfaz abierta y es capaz de trabajar con cualquier lenguaje o plataforma, con clientes en Python y Java, y es accesible a través de una API REST. La escalabilidad también es un beneficio importante que un desarrollador de ML puede aprovechar con MLflow.  El proposito de este cuaderno,  es ver cómo funciona MLflow, con la ayuda de ejemplos y código de muestra. Esto construirá la base necesaria para el resto a fin de utilizar el concepto para diseñar un proyecto de ML de extremo a extremo.

## **¿Qué es MLflow?**
Implementar un producto basado en ML puede ser una tarea laboriosa. Existe una necesidad general de reducir la fricción entre los diferentes pasos del ciclo de vida de desarrollo de ML y entre los equipos de científicos e ingenieros de datos que participan en el proceso.

Los profesionales de ML, como los científicos de datos y los ingenieros de ML, operan con diferentes sistemas, estándares y herramientas. Si bien los científicos de datos pasan la mayor parte de su tiempo desarrollando modelos en herramientas como Jupyter Notebooks, cuando se ejecutan en producción, el modelo se implementa en el contexto de una aplicación de software con un entorno que es más exigente en términos de escala y confiabilidad.

Una ocurrencia común en los proyectos de ML es que un equipo de ingeniería vuelva a implementar los modelos, creando un sistema personalizado para servir al modelo específico. Un conjunto de desafíos son comunes con los equipos que siguen enfoques personalizados con respecto al desarrollo de modelos:
* Proyectos de ML que superan el presupuesto debido a la necesidad de crear una infraestructura de software a medida para desarrollar y servir modelos
* Errores de traducción al reimplementar los modelos producidos por científicos de datos
* Problemas de escalabilidad al entregar predicciones
* Fricción a la hora de reproducir procesos de formación entre científicos de datos por falta de entornos estándar

Las empresas que aprovechan ML tienden a crear sus propios sistemas internos (a menudo extremadamente laboriosos) para garantizar un proceso fluido y estructurado de desarrollo de ML. Las plataformas de ML ampliamente documentadas incluyen sistemas como Michelangelo y FBLearner, de Uber y Facebook, respectivamente.

Es en el contexto de la creciente adopción de ML que MLflow se creó inicialmente en Databricks y de código abierto como plataforma, para ayudar en la implementación de sistemas de ML.

MLflow permite a un profesional diario en una plataforma administrar el ciclo de vida de ML, desde la iteración en el desarrollo del modelo hasta la implementación en un entorno confiable y escalable que es compatible con los requisitos del sistema de software moderno.

## Componetes de MLflow
Los módulos de MLflow son componentes de software que ofrecen las características principales que ayudan en las diferentes fases del ciclo de vida de ML. Las características de MLflow se entregan a través de módulos, componentes extensibles que organizan características relacionadas en la plataforma.

Los siguientes son los módulos integrados en MLflow:
* **Seguimiento de MLflow (MLflow Tracking):** proporciona un mecanismo y una interfaz de usuario para manejar métricas y artefactos generados por ejecuciones de ML (entrenamiento e inferencia)
* **Mlflow Projects:** un formato de paquete para estandarizar proyectos de ML.
* **Modelos Mlflow:** un mecanismo que se implementa en diferentes tipos de entornos, tanto locales como en la nube
* **Registro de modelos de Mlflow:** un módulo que maneja la gestión de modelos en MLflow y su ciclo de vida, incluido el estado.

## **Explorando MLflow tracking**
El componente de MLflow tracking es responsable de la observabilidad. Las características principales de este módulo son el registro de métricas, artifact y parámetros de una ejecución de MLflow. Proporciona visualizaciones y funciones de gestión de artifact.

En una configuración de producción, se usa como un servidor de seguimiento centralizado implementado en Python que puede ser compartido por un grupo de profesionales de ML en una organización. Esto permite que las mejoras en los modelos de ML se compartan dentro de la organización.

El interfaz que registra todas las ejecuciones de su modelo y le permite registrar los observables de su experimento (métricas, archivos, modelos y artifact). Para cada ejecución, puede buscar y comparar las diferentes métricas y parámetros de su módulo.

Aborda los puntos débiles comunes cuando los desarrolladores de modelos comparan diferentes iteraciones de sus modelos en diferentes parámetros y configuraciones.
