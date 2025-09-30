# Lab 3 – Inter-VLAN Routing (Router-on-a-Stick)

## 🎯 Objetivo
Implementar segmentación de red con VLANs y permitir comunicación entre ellas usando Router-on-a-Stick.

## 🖥️ Topología
<img width="1132" height="670" alt="imagen" src="https://github.com/user-attachments/assets/826fe9ea-e698-4615-8feb-1f6c0d774179" />


## 📌 VLANs utilizadas
- VLAN 10 (Docentes) – 172.17.10.0/24
- VLAN 20 (Estudiantes) – 172.17.20.0/24
- VLAN 30 (Invitados) – 172.17.30.0/24

## ⚙️ Configuración

### Router0
```bash
interface g0/0/1
 no shutdown

interface g0/0/1.10
 encapsulation dot1Q 10
 ip address 172.17.10.1 255.255.255.0

interface g0/0/1.20
 encapsulation dot1Q 20
 ip address 172.17.20.1 255.255.255.0

interface g0/0/1.30
 encapsulation dot1Q 30
 ip address 172.17.30.1 255.255.255.0
