# AWS Despliegue de Servidor Web EC2 y Segurdad básica.
---
## Objetivo
Deplegar una máquina virtual (Instancia EC2) Con un servidor web simple (Como Apache o Nginx) y asegurar que solo se pueda acceder a él a través del puerto HTTP (80) desde internet 
---
## Arquitectura Implementada

* **Cómputo (EC2):** Instancia `t2.micro` con Amazon Linux 2
* **Red (VPC) Despliegue en la VPC Default**
* **Seguridad (Security Group):**
  * Regla de Entrada: **SSH (Puerto 22)** solo desde [Tu IP Pública].
  * Regla de Entrada: **HTTP (Puerto 80)** abierta a internet (`0.0.0.0/0`).
* **Automatización:** Script de User Data para la instalación de Apache.
---
## Pasos de Despliegue
