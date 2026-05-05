# 📡 Casio fx-991CW — Guía Completa de Subnetting

> He creado esta Guía práctica para calcular subnetting IPv4 con la calculadora Casio fx-991CW.  
> Incluye fundamentos, conversiones binarias, fórmulas clave y **10 ejercicios resueltos**.

---

## 📄 Contenido del PDF

| Sección | Descripción |
|---------|-------------|
| **0. ¿Qué es Subnetting?** | Definición, analogía, estructura de IPv4 |
| **0.1 Estructura de IPv4** | Los 4 octetos, representación decimal y binaria |
| **0.2 Tabla de bits** | Valores posicionales: 128, 64, 32, 16, 8, 4, 2, 1 |
| **0.3 Máscara de subred** | Qué es, cómo leerla, notación CIDR |
| **0.4 Clases IPv4** | Clase A, B, C y rangos privados RFC 1918 |
| **0.5 Términos clave** | Network, Broadcast, Host válido, Bloque, Prefijo |
| **1. Modo Base-N** | Cómo usar la fx-991CW para conversiones Dec/Bin/Hex |
| **2. Cálculo de máscara** | Fórmula: Bloque = 2^(32-prefijo) |
| **3. Flujo de 5 pasos** | Método universal para cualquier IP/CIDR |
| **4. 10 Ejercicios** | Ejercicios con espacio para resolver |
| **5. Respuestas** | Soluciones detalladas paso a paso |
| **Cheat Sheet** | Todas las fórmulas en una sola página |

---

## 🧮 Fórmulas Clave

```
Bloque          = 2^(32 - prefijo)
Máscara octeto  = 256 - Bloque
Network         = int(IP ÷ Bloque) × Bloque
Broadcast       = Network + Bloque - 1
Hosts útiles    = 2^(32 - prefijo) - 2
```

---

## 📊 Tabla de Referencia Rápida

| CIDR | Máscara          | Bloque | Hosts útiles |
|------|------------------|--------|--------------|
| /24  | 255.255.255.0    | 256    | 254          |
| /25  | 255.255.255.128  | 128    | 126          |
| /26  | 255.255.255.192  | 64     | 62           |
| /27  | 255.255.255.224  | 32     | 30           |
| /28  | 255.255.255.240  | 16     | 14           |
| /29  | 255.255.255.248  | 8      | 6            |
| /30  | 255.255.255.252  | 4      | 2            |

---

## 📝 Ejercicios incluidos

| # | IP / CIDR              | Tipo                        |
|---|------------------------|-----------------------------|
| 1 | 172.16.45.178 / 27     | Clase B — básico            |
| 2 | 10.0.0.200 / 29        | Clase A — /29               |
| 3 | 192.168.10.75 / 28     | Clase C — /28               |
| 4 | 203.0.113.50 / 25      | Clase C — /25               |
| 5 | 172.31.200.130 / 23    | Clase B — supernetting      |
| 6 | 10.10.10.10 / 30       | Clase A — punto a punto     |
| 7 | 192.168.5.220 / 26     | Clase C — /26               |
| 8 | 172.20.100.77 / 22     | Clase B — red grande        |
| 9 | 10.1.1.1 / 8           | Clase A — red completa      |
|10 | 198.51.100.145 / 28    | RFC 5737 — documentación    |

---

## 🖩 Comandos en la Casio fx-991CW

```
MENU → Base-N        Conversiones Dec / Bin / Hex
MENU → Calculate     Operaciones aritméticas
2 [x^y] n            Potencias de 2
```

### Flujo de trabajo rápido

```
1. MENU → Calculate → 2 [x^y] (32 - prefijo)      → Bloque
2. IP_octeto ÷ Bloque → parte entera × Bloque      → Network
3. Network + Bloque - 1                            → Broadcast
4. Network + 1  /  Broadcast - 1                  → Hosts válidos
5. 2 [x^y] (32 - prefijo) - 2                     → Hosts útiles
```

---

## 🎯 Objetivo

Esta guía está orientada a estudiantes que:

- Preparan certificaciones de **networking** (CompTIA Network+, Cisco CCNA)
- Quieren unirse a un **Blue Team** de ciberseguridad
- Aprenden **Kali Linux** y necesitan dominar conceptos de red
- Practican subnetting **sin herramientas digitales** (exámenes con calculadora)

---

## 📁 Archivos en este repositorio

```
.
├── README.md
└── Casio_fx991CW_Subnetting.pdf
```

---

## 🛠 Generado con

- Python 3 + [ReportLab](https://www.reportlab.com/)

---

## 📜 Licencia

Uso libre para fines educativos. Si lo compartes, da crédito al autor original.

---

> *"En ciberseguridad, entender las redes no es opcional — es la base de todo."*
