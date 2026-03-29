# VALAUNI - Sistema de Presupuestos de Aluminio v3.1

## Descripción
Sistema completo de presupuestos para carpintería de aluminio basado en la **Tarifa Aluminios Barcelona 2025**. Calcula el coste real de cada ventana desglosando todos los componentes: marco, hoja, junquillo, herrajes, **fabricación (taller)**, vidrio y montaje — con precio **€/ml** por perfil.

---

## ✅ Funcionalidades Implementadas

### 🪟 Tipos de Ventana / Series (Tarifa Aluminios Barcelona)
| Serie | Tipo | RPT | Perfiles |
|---|---|---|---|
| ALBA PROS 60 | Corredera 2H | ❌ | Marco H/V, Hoja H/V, Junquillo, Refuerzo |
| ALBA PROS 70 | Corredera 2H | ❌ | Marco H/V, Hoja H/V, Junquillo, Refuerzo |
| ALBA PROS 70 RPT | Corredera 2H | ✅ | Marco H/V, Hoja H/V, Junquillo, Refuerzo |
| ALBA PROS 75 RPT | Corredera 2H | ✅ | Marco H/V, Hoja H/V, Junquillo, Refuerzo |
| ALBA PROS 85 RPT | Corredera 2H | ✅ | Marco H/V, Hoja H/V, Junquillo, Refuerzo |
| ALBA A-45 | Practicable 1H | ❌ | Marco H/V, Hoja H/V, Junquillo, Tapajuntas |
| ALBA A-45 (2H) | Practicable 2H | ❌ | Marco H/V, Hoja H/V, Junquillo, Tapajuntas |
| ALFIL 45 RPT | Practicable 1H | ✅ | Marco H/V, Hoja H/V, Junquillo, Tapajuntas |
| ALBA 65 RPT | Practicable 2H | ✅ | Marco H/V, Hoja H/V, Junquillo, Tapajuntas |
| ALFIL OB RPT | Oscilobatiente | ✅ | Marco H/V, Hoja H/V, Junquillo, Tapajuntas |
| ALBA Elevable 120 RPT | Elevable 2H | ✅ | Marco H/V, Hoja H/V, Junquillo, Guía suelo |
| Fijo Estándar | Fijo | ❌ | Marco H/V, Junquillo |

### 💶 Cálculo €/ml por Componente
- **Marco horizontal y vertical**: longitud real calculada de dimensiones
- **Hoja horizontal y vertical**: cálculo según tipo (corredera: ancho/2-30mm; practicable: ancho-40mm)
- **Junquillo**: perímetro de hoja × nHojas
- **Refuerzo/Tapajuntas/Guía suelo**: según serie
- **Juntas EPDM**: perímetro × 1.50€/ml
- **Herrajes**: precio fijo por tipo (corredera_2h, practicable_1h/2h, oscilobatiente, elevable, fijo)
- **Vidrio**: m² útil × precio €/m² (9 tipos disponibles)
- **Montaje**: m² total × precio por tipo (5 opciones)

### 🔄 Desglose Instantáneo
Al seleccionar el tipo de ventana se muestra inmediatamente:
- Tarjetas de componente: Marco / Hoja / Junquillo / Juntas EPDM / Herrajes / Vidrio
- Cada componente muestra: nombre de perfil, código, ml calculados, precio €/ml, subtotal
- Coste por unidad y coste total × cantidad

### 📏 Optimización de Barras (FFD)
- Algoritmo First Fit Decreasing por tipo de perfil
- Separado por: **Marco | Hoja | Junquillo**
- Visual gráfico con barra proporcional por colores
- Indicador % de aprovechamiento (verde/naranja/rojo)

### 🛒 Lista de Compra
- Tabla detallada con: Serie, Componente, Código perfil, Nº barras, €/ml, €/barra, Total
- Total materiales por perfiles

### 💰 Resumen Económico
- Desglose: Material + Montaje = Coste Base
- Margen comercial (Taller +15% / Constructor +20% / Particular +35%)
- Base imponible + IVA 21% = Total

---

## 🗂 Estructura
```
index.html       → Aplicación completa (HTML + CSS + JS)
README.md        → Documentación
```

## 📋 Funcionalidades No Implementadas (próximas versiones)
- [ ] Exportación PDF con logo y datos de empresa
- [ ] Exportación Excel
- [ ] Historial de presupuestos (guardado en base de datos)
- [ ] Colores / acabados del perfil (natural, lacado, anodizado)
- [ ] Importar/exportar presupuesto JSON
- [ ] Configuración de tarifas personalizables
- [ ] Cálculo de persiana/enrollable

## 🔧 Tecnologías
- HTML5 + CSS3 + JavaScript Vanilla
- Font Awesome 6.4 (iconos)
- Google Fonts – Inter
- LocalStorage para guardar presupuestos en navegador
