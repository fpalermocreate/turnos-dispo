# Turnos Libres — Web

## Estructura de archivos

```
turnos-web/
├── login.html        ← pantalla de acceso (entrada principal)
├── turnos.html       ← página de turnos (requiere login)
├── admin.html        ← panel para subir el Excel (solo admin)
├── data/
│   └── turnos.json   ← datos de turnos
└── README.md
```

## Usuarios por defecto

| Usuario    | Contraseña  | Rol                        |
|------------|-------------|----------------------------|
| consulta   | turnos2024  | Ver turnos                 |
| recepcion  | turno2024   | Ver turnos                 |
| admin      | admin123    | Ver turnos + subir Excel   |

**Cambiar contraseñas:** calculá el SHA-256 del nuevo password en
https://emn178.github.io/online-tools/sha256.html y reemplazá el hash
en `login.html` (para viewers) o `admin.html` (para admins).

## Cómo subir a GitHub Pages

1. Crear repo en github.com (ej: `turnos-web`)
2. Subir todos los archivos
3. Settings → Pages → Source: main / root → Save
4. La página queda en: `https://tu-usuario.github.io/turnos-web/login.html`

## Configurar el admin

1. Ir a `/admin.html` y loguearse con `admin / admin123`
2. En "Configuración de GitHub":
   - Crear token en https://github.com/settings/tokens/new (permisos: `repo`)
   - Pegar token, usuario y nombre del repo
   - Guardar configuración
3. A partir de ahí: subir el Excel → Preview → Publicar
