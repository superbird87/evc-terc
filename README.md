# Prompts Vivos (TERC/MSDA + ISM) — Micrositio Online

Micrositio estático (HTML+JS+CSS) que toma un CSV con índices **MSDA/TERC** (IPC, IAE, IIM, IEB, IAB, ICE) y **ISM** (Equidad, Diversidad, Resonancia), y genera **narrativas críticas** en Markdown (prompts vivos).

## Archivos
- `index_online.html`: app web (sin dependencias externas).
- `style.css`: estilos.
- `patrones_semanticos.json`: diccionario de microfrases por rango (alto/medio/bajo/muy_bajo).
- `plantilla_semantica_v1.json`: estructura del texto (bloques).
- `demo_proyectos_TERC_ISM.csv`: ejemplo con 5 casos.

## Usar en local
1. Abre `index_online.html` en tu navegador.
2. Pulsa **Cargar CSV local** o **Cargar demo**.
3. Exporta **Markdown** o **JSONL** con los botones superiores.

## Publicar (GitHub Pages)
1. Crea un repositorio y sube estos archivos a la **raíz**.
2. En *Settings → Pages*, elige **Source = `main`** y **Folder = `/ (root)`**.
3. Espera 1–2 minutos; tendrás una URL pública.  
   - Puedes pasar un CSV por URL: `https://tu-dominio/index_online.html?csv=https://.../archivo.csv`

## Publicar (Netlify/Vercel)
- Arrastra la carpeta al panel o conecta el repo. Listo.

## Formato de CSV
Encabezado obligatorio:
```
Proyecto,IPC,IAE,IIM,IEB,IAB,ICE,Equidad,Diversidad,Resonancia
```

## Personalización
- Ajusta frases en `patrones_semanticos.json` o crea `patrones_semanticos_v1.1.json`.
- Cambia la estructura o textos en `plantilla_semantica_v1.json`.
- Los prompts exportados están en: `prompts.md` (Markdown) y `prompts.jsonl` (JSONL).

## Roadmap
- Validación avanzada del CSV.
- Exportación a PDF A4.
- Persistencia en nube (Supabase/Airtable) con botón **Guardar**.