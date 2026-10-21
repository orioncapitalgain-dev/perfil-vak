# Perfil sensorial VAK

Herramienta web gratuita para estimar si una persona tiene preferencia visual, auditiva o kinestésica. Es una carpeta estática: `index.html` y `assets/` (logo, tipografías e imagen de vista previa), sin dependencias ni servidor.

## Cómo funciona

1. **Cuestionario** (15 situaciones cotidianas, estilo VARK de Fleming y Mills).
2. **Lenguaje** (8 frases con predicados sensoriales, línea de Bandler y Grinder).
3. **Pruebas de desempeño** (visual, auditiva y kinestésica, con corrección por azar). Se muestran como contraste y no entran en el porcentaje del perfil.

El perfil pondera cuestionario y lenguaje según su número de ítems (15 y 8). La lógica y las fuentes están explicadas dentro de la herramienta, en «Fundamento y lógica de las pruebas».

## Marca y calidad

Incluye la marca Cristian Muñoz Mindset (Instagram @CristianMunoz.Mindset) y la colaboración con Orion Academy FXI en el pie, el resultado, el texto copiado y el documento impreso. La bibliografía y el estado de la evidencia están en la propia página. El control de calidad (PHVA) está en `CALIDAD-PHVA.md`.

## Entrega opcional del resultado

Al final, la persona puede escribir su correo o WhatsApp. Se abre su aplicación con el mensaje listo y ella pulsa Enviar. No hay servidor, así que no se guarda ningún dato.

## Privacidad

No hay servidor ni base de datos. Las respuestas no se envían ni se guardan: todo se calcula en el navegador. No se carga nada de servidores de terceros: las tipografías (Barlow e Inter, licencia SIL OFL) van incluidas en `assets/fonts`.

## Publicar en GitHub Pages (Windows PowerShell)

GitHub Pages es gratuito, pero en el plan GitHub Free solo funciona con repositorios **públicos**. El sitio es público aunque el repositorio sea privado (planes de pago).

### Opción A: repositorio propio para la herramienta

1. En GitHub crea un repositorio público llamado `perfil-vak` (sin README).
2. En PowerShell:

```powershell
cd $HOME\Documents
git clone https://github.com/TU_USUARIO/perfil-vak.git
cd perfil-vak
# Copia aquí index.html, .nojekyll y la carpeta assets
git add .
git commit -m "Publica la herramienta Perfil sensorial VAK"
git push origin main
```

3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.
4. En unos minutos (hasta 10) queda en `https://TU_USUARIO.github.io/perfil-vak/`.

### Opción B: dentro de un repositorio existente

```powershell
cd $HOME\Documents\TU_REPOSITORIO
mkdir docs
# Copia index.html, .nojekyll y la carpeta assets dentro de docs
git add docs
git commit -m "Agrega herramienta Perfil sensorial VAK"
git push origin main
```

En **Settings → Pages** elige `main` y la carpeta `/docs`. La dirección será `https://TU_USUARIO.github.io/TU_REPOSITORIO/`.

## Diseño

Tema oscuro con los colores del logotipo de Orion FXI (azul eléctrico y dorado), tipografía Barlow para títulos y Inter para texto, y animaciones suaves al avanzar de pregunta. Respeta la preferencia «reducir movimiento» del sistema. Al imprimir, el documento sale en claro.

## Actualizar

Edita `index.html`, luego:

```powershell
git add .
git commit -m "Actualiza la herramienta"
git push origin main
```

## Límites

La herramienta describe preferencias y rendimiento en pruebas cortas. No es un diagnóstico psicológico ni clínico, y la evidencia de que enseñar según el «estilo» mejore el aprendizaje es débil (Pashler y colegas, 2008). Las pruebas de la parte 3 son diseño propio, sin normas, con un solo intento por canal.
