# Eina de sorteig

Eina web per fer sortejos en directe i gravar-los: rodes o slots animats, amb els participants carregats des d'un fitxer. Tot funciona al navegador, en local: les dades no surten mai de l'ordinador.

Va néixer per als sortejos de la Cursa de Quintos d'Aiguafreda, però serveix per a qualsevol sorteig amb públic.

## Com fer-la servir

No cal instal·lar res: obre `index.html` amb qualsevol navegador modern.

1. **Configura l'aspecte**: títol, logo (el pots reenquadrar des de la pròpia eina), color de fons i color d'accent.
2. **Tria la pantalla**: mode *Rodes* (ruleta) o *Slots*, i quantes en vols (d'1 a 5). Cada roda pot tenir el seu nom i la seva velocitat.
3. **Ajusta el gir**: durada, nombre de franges de la roda i l'animació del guanyador (confeti, focs artificials o xispes).
4. **Defineix les regles**: si una persona pot tenir més d'una participació i si pot guanyar més d'un cop.
5. **Carrega els participants**:
   - Fitxer CSV, TSV, TXT, JSON o Excel (`.xlsx`/`.xls`) amb dues columnes: **nom** i **data**. Les dates `dia/mes/any` s'interpreten amb el dia primer.
   - Opcionalment, una **data màxima** per descartar participacions posteriors.
   - També pots afegir participants addicionals escrits a mà, un per línia.
6. **Previsualitza** amb participants de prova o **crea el sorteig** amb les dades reals.
7. A la pantalla del sorteig, prem **Sorteja**. La tecla **P** amaga el panell per gravar la pantalla neta.

El botó «Carrega l'exemple de la Cursa de Quintos» omple una configuració de mostra amb el logo i els colors de la cursa.

## Detalls tècnics

- Un únic fitxer HTML, sense dependències de build: HTML + CSS + JavaScript a mà.
- L'aleatorietat usa `crypto.getRandomValues` (aleatorietat criptogràfica del navegador).
- Úniques dependències externes: les tipografies de Google Fonts i, només si carregues un Excel, la llibreria SheetJS des de CDN.
- Respecta `prefers-reduced-motion` (animació ràpida si l'usuari l'ha demanada).
- Privacitat: els fitxers de participants es llegeixen localment al navegador; no s'envia res a cap servidor.

## Llicència

Per definir.
