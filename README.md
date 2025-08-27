### Convenciones para nombrar ramas en GitHub

- Usar **minúsculas** y **guiones (-)**  
- Evita espacios, tildes o caracteres especiales.

Ejemplo:
```bash
feature/agregar-login
bugfix/corrige-error-login
hotfix/seguridad-token
```

- **feature/** → para nuevas funcionalidades  
```bash
feature/registro-usuarios
```

- **bugfix/** → para correcciones de errores no críticos  
```bash
bugfix/validacion-formulario
```

- **hotfix/** → para arreglos urgentes en producción  
```bash
hotfix/corregir-nullpointer
```

- **release/** → para preparar una versión  
```bash
release/v1.2.0
```

- **experiment/** → para pruebas o prototipos  
```bash
experiment/nueva-ui
```

- Nombre corto pero significativo (evitar genéricos como `fix`, `temp`, `test`)  
```bash
feature/exportar-reporte-pdf
```

- Opcional: incluir número de issue/ticket (si usas Jira, GitHub Issues, Trello, etc.)  
```bash
feature/123-agregar-login
bugfix/456-corrige-validacion
```

---

🔄 **Flujos de trabajo recomendados**

1. **Git Flow (clásico)**  
   - Ideal para proyectos grandes:  
   - `main` (producción, siempre estable)  
   - `develop` (última versión en desarrollo)  
   - Ramas temporales: `feature/*`, `bugfix/*`, `release/*`, `hotfix/*`  

2. **GitHub Flow (simple)**  
   - Ideal para proyectos pequeños o ágiles:  
   - `main` (solo código listo para producción)  
   - Para cada cambio → rama `feature/...` o `fix/...`  
   - Se hace **Pull Request** hacia `main`  

3. **Trunk Based Development**  
   - Muy usado en CI/CD:  
   - `main` siempre está desplegable  
   - Ramas cortas (horas o pocos días), se integran rápido  

---

✅ **Buenas prácticas adicionales**  
- Una rama = un objetivo claro (no mezclar varias cosas).  
- Commits pequeños y claros, con mensajes significativos.  
- Mantener ramas cortas: mientras menos vivan, menos conflictos.  
- Eliminar ramas después de hacer merge (para no llenar el repo).  
- Revisar antes de merge: usar Pull Requests con revisión de código.  

---

👉 **Ejemplo de flujo sencillo en GitHub Flow:**  

Crear rama para la tarea:  
```bash
git checkout -b feature/agregar-login
```

Trabajar en ella, hacer commits.  

Subirla:  
```bash
git push origin feature/agregar-login
```

Crear un Pull Request hacia `developer` o `main` dependiendo de cual este en uso.  
Revisar, aprobar y hacer merge.  
Borrar la rama.
