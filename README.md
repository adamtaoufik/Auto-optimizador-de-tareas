# ⚙️ Gestor de Procesos en Python

> Herramienta CLI para monitorizar procesos y eliminar procesos zombie en Linux.

---

## 🧠 Funcionalidad

Script simple orientado a **gestión de procesos**, con foco en estabilidad del sistema:

- 📋 Listado de procesos activos
- 🧟 Detección de procesos zombie
- ❌ Eliminación manual de procesos (kill)
- 🧑‍💻 Menú interactivo en consola

---

## 🔍 Qué hace exactamente

- Itera todos los procesos con `psutil`
- Muestra:
  - PID
  - Nombre
  - Estado
- Detecta procesos en estado `ZOMBIE`
- Permite eliminarlos bajo demanda

---

## 🏗️ Arquitectura

main()
 ├── analizar_processos()  # Lista + detecta zombies
 └── kill_process(pid)    # Mata procesos por PID

---

## ⚙️ Requisitos

- Python 3.x  
- psutil:
  ```bash
  pip install psutil
  ```

---

## ▶️ Ejecución

```bash
python3 script.py
```

---

## 🧪 Casos de uso

- Diagnóstico de procesos colgados
- Limpieza de zombies
- Administración básica de sistema Linux

---

## ⚠️ Consideraciones

- Usa `kill` → requiere permisos adecuados
- Puede afectar procesos críticos si se usa mal
- No hay validación avanzada de PID (mejorable)

---

## 🧩 Mejoras futuras

- Validación de input
- Uso de `kill -9` opcional
- UI más avanzada (TUI tipo htop)
- Logs de acciones
- Filtros por proceso

---

## 👨‍💻 Autor

Adam Taoufik Ezouhari
