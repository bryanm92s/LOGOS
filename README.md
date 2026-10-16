# LOGOS — logos públicos de los proyectos 🔓

Repo **público a propósito**: guarda los logos de cada proyecto para que
los repos de código puedan ser **privados** sin romper las imágenes.

**Por qué existe:** cuando un repo de GitHub pasa a privado, sus archivos
dejan de ser accesibles por URL cruda (`raw.githubusercontent.com`).
Si `VITE_BIZ_LOGO` apunta al repo privado, el logo desaparece de la app.
Apuntando **aquí** (público), el logo sigue funcionando con los repos
cerrados.

## URLs listas para usar

Copia la URL en **Vercel → Settings → Environment Variables →
`VITE_BIZ_LOGO`** (y recuerda: después hay **Redeploy**, las `VITE_*` se
incrustan al compilar).

| Proyecto | Archivo | URL raw |
|---|---|---|
| SZ (micropigmentación) | `LOGO-SZ/logo-sz.png` | `https://raw.githubusercontent.com/bryanm92s/LOGOS/main/LOGO-SZ/logo-sz.png` |
| WXYZ (spa de uñas) | `LOGO-NAIL/logo-nail_.png` | `https://raw.githubusercontent.com/bryanm92s/LOGOS/main/LOGO-NAIL/logo-nail_.png` |
| BARBERIA | `LOGO-BARBERIA/logo-barberia_.png` | `https://raw.githubusercontent.com/bryanm92s/LOGOS/main/LOGO-BARBERIA/logo-barberia_.png` |

> 📌 El `logo.png` de la **raíz del repo** del proyecto es otra cosa: es
> el `apple-touch-icon` que sirve **Vercel desde el build** (no desde
> GitHub), así que ese sí funciona igual con el repo privado. Este repo
> es solo para la URL externa (`VITE_BIZ_LOGO`) y otros usos fuera.

## ¿Logos de pago (Nequi, Daviplata, Bancolombia)?

No están aquí: son archivos genéricos dentro de cada proyecto
(`public/img/pagos/`) que **Vercel sirve desde el build**. Con el repo
privado siguen visibles en la app, no hay nada que mover.

## Agregar el logo de un cliente nuevo

1. Sube la imagen en una carpeta con su nombre:
   `LOGO-<CLIENTE>/logo-<cliente>.png`
2. Commit + push.
3. Agrega la fila en la tabla de arriba con su URL raw.
4. Pega esa URL en `VITE_BIZ_LOGO` del proyecto del cliente.
