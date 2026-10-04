# 💳 Proyecto SQL: Alke Wallet

Este proyecto consiste en el diseño y creación de una base de datos relacional para gestionar un sistema de billetera virtual (Wallet). Permite a los usuarios almacenar fondos, realizar transacciones y consultar su historial financiero.

## 🎯 Objetivo
Diseñar el modelo conceptual, definir las relaciones entre entidades y crear la base de datos aplicando sentencias DDL, DML y TCL (Transacciones ACID) utilizando **MySQL 8.0**.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** SQL (MySQL 8.0)
* **Herramientas:** DB-Fiddle, Visual Studio Code, dbdiagram.io

## 📊 Modelo Entidad-Relación (ERD)

<img width="796" height="437" alt="image" src="https://github.com/user-attachments/assets/53323317-5f89-4028-9258-27e07fe68fc0" />


**Descripción del Modelo:**
* **Relación Usuario - Transacción (1:N):** Un usuario puede participar en múltiples transacciones, ya sea enviando o recibiendo fondos. La tabla transacción utiliza `sender_user_id` y `receiver_user_id` como llaves foráneas.
* **Relación Moneda - Transacción (1:N):** Una moneda específica (CLP, USD, etc.) puede ser utilizada en múltiples transacciones.
* **Normalización:** El modelo se encuentra en Tercera Forma Normal (3FN), eliminando redundancias y asegurando que cada dato dependa únicamente de su clave primaria.

## 🚀 Funcionalidades Implementadas
El archivo `AlkeWallet.sql` incluido en este repositorio contiene los scripts para:
1. Creación de la base de datos y tablas (`CREATE`).
2. Carga inicial de usuarios, monedas y transacciones (`INSERT`).
3. Actualización y eliminación de registros (`UPDATE`, `DELETE`).
4. Consultas relacionales utilizando `JOIN` para obtener historiales detallados.
5. Simulaciones de seguridad financiera aplicando principios **ACID** (`START TRANSACTION`, `COMMIT`, `ROLLBACK`).

---
**Arquitectura y Diseño de Datos por:**  
Benjamín Alonso Carmona Vega — Desarrollador Backend & Database Designer  
https://www.iasesoria.cl
