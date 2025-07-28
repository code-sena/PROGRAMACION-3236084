# Ejercicios prácticos: Especificación de Requisitos con PlantUML (WSD)

A continuación, encontrarás ejemplos de diagramas en formato WSD (Wire Sequence Diagram) que puedes visualizar y modificar usando [PlantUML](https://plantuml.com/es/), [PlantText](https://www.planttext.com/) o extensiones de VS Code como PlantUML:

## 1. Diagrama de Casos de Uso
Archivo: `ejercicio_casos_uso.wsd`
```wsd
@startuml casos_uso
actor Cliente
actor Administrador
Cliente --> (Registrarse)
Cliente --> (Buscar productos)
Cliente --> (Agregar al carrito)
Cliente --> (Realizar compra)
(Realizar compra) --> (Pagar)
Administrador --> (Gestionar productos)
Administrador --> (Ver reportes)
@enduml
```

## 2. Diagrama de Arquitectura General
Archivo: `ejercicio_arquitectura.wsd`
```wsd
@startuml arquitectura_general
package "Frontend" {
  [WebApp]
}
package "Backend" {
  [API REST]
  [Autenticación]
}
package "Base de Datos" {
  [DB MySQL]
}
[WebApp] --> [API REST] : HTTP/HTTPS
[API REST] --> [Autenticación]
[API REST] --> [DB MySQL]
@enduml
```

## 3. Diagrama de Flujo de Interacción
Archivo: `ejercicio_flujo_interaccion.wsd`
```wsd
@startuml flujo_interaccion
actor Cliente
participant "WebApp" as Web
participant "API REST" as API
participant "DB MySQL" as DB
Cliente -> Web: Selecciona producto
Web -> API: Solicita detalles producto
API -> DB: Consulta producto
DB --> API: Retorna datos
API --> Web: Retorna detalles
Cliente -> Web: Agrega al carrito
Web -> API: Envía carrito
API -> DB: Guarda carrito
Cliente -> Web: Realiza compra
Web -> API: Solicita compra
API -> DB: Registra compra
API --> Web: Confirmación
Web --> Cliente: Muestra confirmación
@enduml
```

Puedes abrir estos archivos en PlantUML para ver los diagramas y modificarlos según tus necesidades. Si tienes dudas sobre cómo instalar o usar PlantUML, te puedo orientar.

