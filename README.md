# 🛒 MiniTienda - Sistema de Gestión de Ventas e Inventario

<p align="center">
  <img src="https://img.shields.io/badge/Laravel-12.x-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel">
  <img src="https://img.shields.io/badge/PHP-8.x-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind">
</p>

---

## 📌 Información General

* **Proyecto:** MiniTienda
* **Tipo de Aplicación:** Sistema Web de Gestión de Ventas e Inventario
* **Framework:** Laravel 12
* **Lenguaje:** PHP 8.x
* **Base de Datos:** MySQL
* **Frontend:** Blade + Tailwind CSS
* **Control de Acceso:** Spatie Laravel Permission

---

## 📖 Descripción del Proyecto

**MiniTienda** es una aplicación web desarrollada para administrar de forma eficiente las operaciones de una tienda comercial. 

El sistema permite gestionar productos, categorías, inventario, ventas, usuarios y compras en línea mediante un carrito de compras. Además, incorpora un sistema de autenticación y autorización basado en roles para garantizar la seguridad y el control de acceso.

La aplicación fue desarrollada siguiendo el patrón **MVC (Modelo - Vista - Controlador)** proporcionado por Laravel.

---

## 🎯 Objetivos del Sistema

### Objetivo General
Desarrollar un sistema web que permita administrar los procesos de inventario, ventas y usuarios de una tienda utilizando Laravel y MySQL.

### Objetivos Específicos
* 📦 Gestionar productos y categorías.
* 📉 Controlar existencias de inventario.
* 💰 Registrar ventas realizadas.
* 🛒 Implementar carrito de compras.
* 👥 Administrar usuarios mediante roles.
* 🛍 Permite el seguimiento de compras realizadas por clientes.
* 🔐 Aplicar control de acceso basado en permisos.

---

## 🏗 Arquitectura del Sistema

El sistema utiliza la arquitectura estándar **MVC**, estructurada de la siguiente manera:

| 🗄️ Modelos | ⚙️ Controladores | 🎨 Vistas |
| :--- | :--- | :--- |
| • User<br>• Product<br>• Category<br>• Sale<br>• SaleDetail | • ProductController<br>• CategoryController<br>• CartController<br>• StoreController<br>• UserController<br>• ProfileController | • Dashboard Administrativo<br>• Gestión de Productos / Categorías<br>• Gestión de Usuarios<br>• Tienda Virtual<br>• Carrito de Compras<br>• Historial de Compras |

---

## 👥 Roles y Funciones del Sistema

### 👑 Administrador
> Tiene acceso total al sistema.
* **Gestión de Usuarios:** Crear, editar, eliminar y asignar roles.
* **Gestión de Catálogo:** Control total sobre productos y categorías.
* **Operaciones:** Monitoreo y control de inventario y ventas.

### 📦 Gestor de Inventario
> Responsable del control operativo del inventario.
* **Productos:** Registrar, modificar y eliminar artículos.
* **Organización:** Gestionar categorías y actualización de stock en tiempo real.
* **Consultas:** Acceso a la visualización y reporte de ventas.

### 🛍️ Cliente
> Usuario final de la tienda virtual.
* **Acceso:** Registro e inicio de sesión seguro.
* **Compra:** Consultar productos, interactuar con el carrito y procesar el pago.
* **Seguimiento:** Consulta detallada de su historial de pedidos.

---

## 🧩 Módulos Principales

### 📦 Módulo de Inventario
Permite administrar todos los productos de la tienda de forma centralizada.
* CRUD completo de productos (Crear, Editar, Eliminar, Consultar).
* Control automatizado de stock disponible.
* Clasificación y organización por categorías.

### 💰 Módulo de Ventas & Carrito
Soporta el flujo comercial desde la selección hasta el despacho.
* **Carrito de compras:** Agregar, eliminar y previsualizar el resumen del pedido.
* **Procesamiento:** Registro automático de la venta y generación de detalles.
* **Automatización:** Cálculo de totales y rebaja automatizada del stock.

### 👤 Módulo de Usuarios & Seguridad
Garantiza que cada usuario acceda únicamente a lo que le corresponde.
* Administración y asignación de roles.
* Gestión de permisos específicos mediante **Spatie Permission**.

---

## 📊 Base de Datos (Tablas Principales)

* **Autenticación y Roles:** `users`, `roles`, `permissions`, `model_has_roles`, `model_has_permissions`, `role_has_permissions`.
* **Inventario:** `products`, `categories`.
* **Ventas:** `sales`, `sale_details`.

---

## 🔐 Seguridad Implementadas

* [x] Autenticación de usuarios segura.
* [x] Middleware de autorización por rutas y controladores.
* [x] Control de acceso basado en roles (RBAC) con Spatie.
* [x] Protección contra ataques CSRF.
* [x] Validaciones estrictas en formularios de Request.


### 1. Clonar el repositorio
```bash
git clone URL_DEL_REPOSITORIO
cd minitienda
---
###2. Instalar dependencias de PHP
Bash
composer install
---
####3. Configurar el entorno
Bash
cp .env.example .env
---
####4.Abre el archivo .env y configura las credenciales de tu base de datos local:

Fragmento de código
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=minitienda
DB_USERNAME=root
DB_PASSWORD=
#####5. Inicializar la aplicación
Bash
# Generar la clave de la aplicación
php artisan key:generate

# Ejecutar migraciones y seeders
php artisan migrate --seed

# Crear el enlace simbólico para el almacenamiento de imágenes
php artisan storage:link
######6. Compilar Assets y lanzar el servidor
En terminales separadas, ejecuta:

Bash
# Servidor de desarrollo de Laravel
php artisan serve

# Compilación de estilos con Vite
npm install
npm run dev
---


📚 Tecnologías Utilizadas
Backend: Laravel 12 & PHP 8

Base de Datos: MySQL

Frontend: Blade Components & Tailwind CSS

Autenticación Starter Kit: Laravel Breeze

Permisos: Spatie Laravel Permission

Gestores de Paquetes: Composer & Vite
