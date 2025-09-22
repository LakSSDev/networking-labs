# Laboratorio de Subnetting con VLSM en Packet Tracer

## 🎯 Objetivo
Diseñar y configurar 3 subredes usando VLSM, asignando gateways en el router y verificando conectividad.

## 🖥️ Topología
(Insertar aquí la imagen exportada de Packet Tracer, por ejemplo topologia.png)

## 📊 Tabla de Direcciones IP
| Subred       | Prefijo | Gateway       | Rango de Hosts        | Broadcast   |
|--------------|---------|---------------|-----------------------|-------------|
| 10.0.0.0/26  | /26     | 10.0.0.1      | 10.0.0.1 – 10.0.0.62  | 10.0.0.63   |
| 10.0.0.64/27 | /27     | 10.0.0.65     | 10.0.0.65 – 10.0.0.94 | 10.0.0.95   |
| 10.0.0.96/28 | /28     | 10.0.0.97     | 10.0.0.97 – 10.0.0.110| 10.0.0.111  |

## ⚙️ Configuración del Router (Cisco IOS)
```bash
enable
configure terminal

interface gigabitEthernet 0/0
 ip address 10.0.0.1 255.255.255.192
 no shutdown
exit

interface gigabitEthernet 0/1
 ip address 10.0.0.65 255.255.255.224
 no shutdown
exit

interface gigabitEthernet 0/2
 ip address 10.0.0.97 255.255.255.240
 no shutdown
exit
```

## ✅ Pruebas de Conectividad
- PC0 ping a PC2 → ✅ responde  
- PC1 ping a PC5 → ✅ responde  
- PC3 ping a PC4 → ✅ responde  

## 📌 Conclusión
Con VLSM logré dividir una red /24 en subredes más pequeñas (/26, /27 y /28),
optimizando direcciones IP y garantizando comunicación entre segmentos de red usando un router como gateway.

<img width="1329" height="542" alt="Topologia" src="https://github.com/user-attachments/assets/528bf646-6dd0-4930-a513-c4aee5849f75" />


