# Práctica de chino

Sitio estático para practicar chino mediante **tarjetas de estudio** y **reconocimiento auditivo de frases**, inspirado en una dinámica similar a AnkiWeb.

## Funcionalidades

- Selección de una o varias lecciones o lotes
- Elección de tipo de práctica:
  - **Tarjetas**
  - **Audios**
- En modo **Tarjetas**:
  - visualización de hanzi
  - revelado de pinyin, significado y oración de ejemplo
- En modo **Audios**:
  - reproducción de frases mediante síntesis de voz
  - reconocimiento auditivo antes de revelar la respuesta
  - selector visible de velocidad de reproducción
- Marcado de ítems como:
  - **La sabía**
  - **No la sabía**
- Lote automático de ítems **a repasar**
- Opción de repasar pendientes al finalizar
- Reinicio de ronda o de lección
- Guardado de progreso en `localStorage`

## Tecnologías

- HTML
- CSS
- JavaScript puro

No requiere backend ni base de datos.

## Estructura

Los datos están embebidos dentro del mismo `index.html`, en un objeto `APP_DATA`.

Actualmente hay dos tipos principales de lotes:

- `lessons`: tarjetas de vocabulario / caracteres
- lotes de frases (`leccion-4-frases` en adelante): usados para práctica de audio

### Ejemplo de tarjeta

```js
{
  id: "l1-001",
  hanzi: "你",
  pinyin: "nǐ",
  meaning: "tú",
  example_hanzi: "你好。",
  example_pinyin: "Nǐ hǎo.",
  example_es: "Hola."
}
