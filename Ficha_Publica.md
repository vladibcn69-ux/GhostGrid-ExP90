# Ficha pública — GhostGrid (Boot2Root)

**Módulo:** MF0490_3 — Administración de sistemas informáticos
**Autor:** Volodymyr Osebchuk
**Tipo:** Máquina vulnerable intencionada · Boot2Root
**Dificultad:** Fácil–media

## Escenario

GhostGrid es el servidor de una **comunidad/portal OSINT ficticio**. La máquina
se ha preparado como reto **Boot2Root**: el jugador parte de una máquina atacante
en la misma red y debe hacerse con el control total del sistema.

## Objetivo

Conseguir un **acceso inicial** al sistema como usuario sin privilegios y, a
partir de ahí, una **escalada de privilegios local hasta `root`**. El reto se
considera superado al capturar las dos banderas:

- `user.txt` — demuestra el acceso inicial.
- `root.txt` — demuestra el control total (root).

Formato de las banderas: `GHOSTGRID{...}`.

## Información general

- **Servicios expuestos:** un servicio **web (HTTP)** y acceso **SSH**.
- **Punto de partida:** máquina atacante en la misma red (por ejemplo, Kali).
  No se requieren exploits de kernel, fuerza bruta ni fuga de contenedor.
- **Recorrido (alto nivel):** enumeración → acceso inicial sin privilegios →
  escalada local → `root`. La ruta prevista es única y reproducible.
- **Persistencia:** el reto se mantiene tras reiniciar la máquina.

## Habilidades que se practican

- Enumeración de servicios de red (web y SSH).
- Enumeración del sistema local y detección de configuraciones incorrectas.
- Escalada de privilegios en Linux.

## Despliegue

- Imagen portable en formato **OVA** (importable en VirtualBox) y/o sala en
  **TryHackMe**.
- La red se configura por **DHCP**; la IP se obtiene en el arranque.

## Notas

- Esta ficha es **pública** y **no** contiene vulnerabilidades concretas,
  contraseñas, banderas ni la solución del reto (sin *spoilers*).
- La solución detallada, las credenciales y los valores de referencia se
  entregan por separado en el **dossier privado del creador** (solo para el docente).
