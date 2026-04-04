---
{"dg-publish":true,"permalink":"/personas/","dg-note-properties":{}}
---

📇 PLANTILLA — LISTADO DE PERSONAS
Markdown
# 👥 Personas

> [!info]
> Índice general de todas las personas dentro del sistema.

---

## 🔎 Todas las personas
```dataview
table 
  nombre as "Nombre",
  alias as "Alias",
  ocupacion as "Ocupación",
  estado as "Estado"
from "Personas"
where tipo = "persona"
sort nombre asc
🟢 Personas activas
Dataview
list 
from "Personas"
where tipo = "persona" and estado = "activo"
sort nombre asc
📜 Personas históricas
Dataview
list
from "Personas"
where tipo = "persona" and estado = "historico"
sort nombre asc
⭐ Personas destacadas
Dataview
table nombre, importancia
from "Personas"
where tipo = "persona" and importancia = "alta"
sort nombre asc
🧩 Personas por rol
Dataview
table rol, length(rows) as "Cantidad"
from "Personas"
where tipo = "persona"
group by rol
📊 Estadísticas
Dataview
table length(rows) as "Cantidad"
from "Personas"
where tipo = "persona"
group by estado
🧭 Navegación
[[Personas activas\|Personas activas]]
[[Personas históricas\|Personas históricas]]
[[Relaciones\|Relaciones]]