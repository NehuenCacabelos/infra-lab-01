# 🌐 Topología de Red: Laboratorio "Pollos Hermanos"

Este documento detalla la infraestructura de red y el inventario de máquinas que componen el laboratorio **infra-lab-01**.

## 📍 Arquitectura Lógica
El laboratorio simula una red corporativa con servicios de directorio, servidores de tareas y estaciones de trabajo cliente.



## 🛠️ Inventario de Nodos (Infraestructura)

| Nombre Clave | Sistema Operativo | Rol / Función | Red |
| :--- | :--- | :--- | :--- |
| **Blue-Sky** | Windows Server 2022 | **Active Directory** (Dominio: pollos.hermanos) | Gestión / Interna |
| **Methylamine** | Ubuntu Server | Servidor de Tareas y Procesos | Interna |
| **Ricin** | Windows 10 | Cliente de Usuario Final | Interna |

## 🌐 Servicios de Red y Resolución de Nombres (DNS)

En la configuración actual, el nodo **Blue-Sky** centraliza la identidad y la red del laboratorio.

* **DNS Primario (Nodos):** Apuntan a la IP de **Blue-Sky**. Esto permite que `Methylamine` y `Ricin` reconozcan el dominio `pollos.hermanos`.
* **Dominio:** `polloshermanos.local` (o el que hayas configurado).

### Flujo de Resolución:
`Nodo` ⮕ `Blue-Sky (DNS Local)` ⮕ `8.8.8.8 (Internet)`


## 📸 Diagrama de red
![Topologia de redl](../assets/capturas/Diagrama-de-red.png)

---
**Última actualización:** 12 de enero de 2026
