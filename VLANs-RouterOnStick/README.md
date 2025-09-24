# Laboratorio VLANs y Router-on-a-Stick

## 🎯 Objetivo
Configurar VLANs en un switch Cisco y usar un Router-on-a-Stick para permitir comunicación entre dos VLANs.

## 🖥️ Topología
- Switch 2950
- Router 2911
- 4 PCs
- VLAN 10: Administración (192.168.10.0/24)
- VLAN 20: Ventas (192.168.20.0/24)

![Topologia](topologia.png)

## 📊 Tabla de direcciones
| VLAN | Subred           | Gateway       | PCs asignados         |
|------|------------------|---------------|-----------------------|
| 10   | 192.168.10.0/24  | 192.168.10.1  | PC0 (10.10), PC1 (10.11) |
| 20   | 192.168.20.0/24  | 192.168.20.1  | PC2 (20.10), PC3 (20.11) |

## ⚙️ Configuración del Switch
Ver archivo [`config_switch.txt`](config_switch.txt)

## ⚙️ Configuración del Router
Ver archivo [`config_router.txt`](config_router.txt)

## ✅ Pruebas
- Ping entre PC0 ↔ PC1 (OK)  
- Ping entre PC2 ↔ PC3 (OK)  
- Ping entre PC0 ↔ PC2 (OK, vía router)  

## 📌 Conclusión
Se configuraron VLANs y un Router-on-a-Stick para lograr comunicación entre dos departamentos virtualmente separados dentro de un mismo switch.
