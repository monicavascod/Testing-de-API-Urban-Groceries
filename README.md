<div align="center">

# 🛠 Testing de API: Urban Groceries  

📌 **Rol:** QA Manual  
📌 **Objetivo:** Validar la **API de Urban Groceries**, enfocándose en la creación de kits personalizados y la lógica del servicio de entregas **Order and Go**.  

</div>

---

## 📑 Descripción
Este proyecto consistió en diseñar y ejecutar **50 casos de prueba** para la API REST de Urban Groceries.  
Se validaron escenarios positivos y negativos para:  

- Creación, modificación y eliminación de **kits personalizados** (`/api/v1/kits/:id/products`).  
- Validación de **restricciones de nombres e IDs**.  
- Manejo de errores por **inputs inválidos y estructuras incorrectas**.  
- Lógica de cálculo de entregas (`/order-and-go/v1/delivery`).  
- Reglas de negocio: **horarios permitidos, cantidad de productos y peso máximo**.  

---

## 🧰 Stack y Herramientas
<p align="center">
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white"/>
  <img src="https://img.shields.io/badge/REST%20API-25D366?style=for-the-badge&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white"/>
</p>

---

## 🔹 Requisito 1: `/api/v1/kits/:id/products`

- ✅ Casos positivos:  
  - Crear kit válido.  
  - Agregar productos existentes.  
  - Modificar nombre de kit.  
  - Eliminar kit.  
- ❌ Casos negativos detectados:  
  - Validación incorrecta de nombre (hebreo, caracteres especiales, longitud).  
    - [UG-1](https://monivascod.atlassian.net/browse/UG-1)  
    - [UG-2](https://monivascod.atlassian.net/browse/UG-2)  
    - [UG-3](https://monivascod.atlassian.net/browse/UG-3)  
    - [UG-4](https://monivascod.atlassian.net/browse/UG-4)  
  - Fallos con IDs inválidos (letras, negativos, caracteres especiales).  
    - [UG-6](https://monivascod.atlassian.net/browse/UG-6)  
    - [UG-7](https://monivascod.atlassian.net/browse/UG-7)  
  - Manejo incorrecto de `quantity` y `productsList`.  
    - [UG-13](https://monivascod.atlassian.net/browse/UG-13)  
    - [UG-15](https://monivascod.atlassian.net/browse/UG-15)  
    - [UG-8](https://monivascod.atlassian.net/browse/UG-8)  

---

## 🔹 Requisito 2: `/order-and-go/v1/delivery`

- ✅ Casos positivos:  
  - Entregas válidas dentro de rango de horario (08–22).  
  - Validaciones correctas en peso y cantidad de productos dentro del rango permitido.  

- ❌ Casos negativos detectados:  
  - Fallos en validación de horario fuera de rango o inválido.  
    - [UG-5](https://monivascod.atlassian.net/browse/UG-5)  
    - [UG-9](https://monivascod.atlassian.net/browse/UG-9)  
    - [UG-10](https://monivascod.atlassian.net/browse/UG-10)  
    - [UG-11](https://monivascod.atlassian.net/browse/UG-11)  
    - [UG-12](https://monivascod.atlassian.net/browse/UG-12)  
    - [UG-14](https://monivascod.atlassian.net/browse/UG-14)  
    - [UG-16](https://monivascod.atlassian.net/browse/UG-16)  
  - Errores en validación de cantidad y peso de productos.  
    - [UG-17](https://monivascod.atlassian.net/browse/UG-17)  
    - [UG-18](https://monivascod.atlassian.net/browse/UG-18)  
    - [UG-19](https://monivascod.atlassian.net/browse/UG-19)  
    - [UG-20](https://monivascod.atlassian.net/browse/UG-20)  
    - [UG-21](https://monivascod.atlassian.net/browse/UG-21)  
    - [UG-22](https://monivascod.atlassian.net/browse/UG-22)  
    - [UG-23](https://monivascod.atlassian.net/browse/UG-23)  
    - [UG-24](https://monivascod.atlassian.net/browse/UG-24)  
    - [UG-25](https://monivascod.atlassian.net/browse/UG-25)  
    - [UG-26](https://monivascod.atlassian.net/browse/UG-26)  
    - [UG-27](https://monivascod.atlassian.net/browse/UG-27)  
    - [UG-28](https://monivascod.atlassian.net/browse/UG-28)  
    - [UG-29](https://monivascod.atlassian.net/browse/UG-29)  
    - [UG-30](https://monivascod.atlassian.net/browse/UG-30)  
    - [UG-31](https://monivascod.atlassian.net/browse/UG-31)  
    - [UG-32](https://monivascod.atlassian.net/browse/UG-32)  

---

## 📊 Resultados
- Se diseñaron y ejecutaron **50 casos de prueba**.  
- **Hallazgos clave:**  
  - La API no valida correctamente caracteres no permitidos, IDs inválidos y límites en `quantity`.  
  - El servicio `/order-and-go/v1/delivery` acepta valores fuera de rango (horarios, cantidad y peso).  
- Todos los defectos fueron documentados en **Jira** para seguimiento.  

---

<div align="center">

✨ Proyecto desarrollado como parte de mi formación en **QA Manual (API Testing)**.  
🔗 [Ver mi perfil de GitHub](https://github.com/monicavascod)  

</div>
