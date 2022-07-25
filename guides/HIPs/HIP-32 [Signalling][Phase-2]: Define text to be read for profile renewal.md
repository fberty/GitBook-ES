# HIP-32 [Signalling][Phase-2]: Define text to be read for profile renewal
```
HIP: 32
title: Define text to be read for profile renewal.
author: ludoviko
status: Phase 2
created: 2021-10-24

```

# Simple summary
Clarify what the phrase should be for renewal of the profile. 

# Abstract
Now that the renewal period has begun for some, there are some issues regarding the phrase that should be used for renewal. Current phrase states "...and that I am not already registered in this registry" which would be false for already registered users. The primary aim for this proposal would be to clearly define what the phrase should be.

# Motivation
The renewals beginning in the following month is going to trigger more opportunistic challenges due to lack of clarification of the current text.

# Specification
An upgrade to the metadata document should be added which will specify the renewal procedure.
Add a section with title "Elements required for renewal" and say

> The renewal procedure will follow the same rules than the registry procedure **except:**
> * The renewer must say <to be defined, see below>. Renewers should speak in their normal voice and should not attempt mimicking someone else’s voice. Speaking before or after the required sentence is acceptable. Poor English accents, mispronunciations, and the switch or oversight of words in that sentence are not grounds for rejections
> * The sign should display in a readable manner the <time validation options, se below> 

## Proposed new phrases in English
- “I certify that I am a real human and that I am renewing my registration on this registry” by @juanu
- “I certify that I am a real human and that I am re-applying for this registry” by @Koki
- "“I certify that I am a real human, and this is my video for Proof of Humanity.” by @ruben

## Proposed alternatives for time validation
The sign should show an ethereum blockhash, which could be 
* the time when the renewer clicked on the "renew" button. 
* some periodical reference time in the recent past, for example the midnight UTC of last day, or 00:01:00 UTC of the first day of each month. 

The way that this time validation is generated should be less mistake-prone for the renewer, and easier/faster for the challenger to catch a mismatch. A solution that could prevent long character strings is to shorten the hash into an even shorter hash through some shortening algorithm. Ideally it would consist of 4-6 characters.

---
# Resumen simple
Aclarar cuál debe ser la frase para la renovación del perfil. 

# Resumen
Ahora que ha comenzado el periodo de renovación para algunos, hay algunas cuestiones relacionadas con la frase que debe utilizarse para la renovación. La frase actual dice "...y que no esté ya inscrito en este registro" lo cual sería falso para los usuarios ya registrados. El objetivo principal de esta propuesta sería definir claramente cuál debe ser la frase.

# Motivación
Las renovaciones que comienzan en el mes siguiente van a desencadenar más impugnaciones oportunistas debido a la falta de aclaración del texto actual.

# Especificación
Debería añadirse una actualización del documento de metadatos que especifique el procedimiento de renovación.
Añadir una sección con el título "Elementos necesarios para la renovación" y decir

> El procedimiento de renovación seguirá las mismas reglas que el procedimiento de registro **excepto:** > El renovador debe decir <a definir, véase más adelante>. Los renovadores deben hablar con su voz normal y no deben intentar imitar la voz de otra persona. Se acepta hablar antes o después de la frase requerida. El acento inglés deficiente, la mala pronunciación y el cambio u omisión de palabras en esa frase no son motivo de rechazo
> * El cartel debe mostrar de manera legible las <opciones de validación de tiempo, se abajo> 

## Nuevas frases propuestas en inglés
- "Certifico que soy un humano real y que renuevo mi inscripción en este registro" por @juanu
- "Certifico que soy un humano real y que vuelvo a solicitar mi inscripción en este registro" por @Koki
- "Certifico que soy un humano real y que este es mi vídeo para la Prueba de Humanidad" por @ruben

## Alternativas propuestas para la validación del tiempo
El cartel debería mostrar un blockhash de ethereum, que podría ser 
* la hora en que el renovador hizo clic en el botón "renovar". 
* alguna hora de referencia periódica en el pasado reciente, por ejemplo la medianoche UTC del último día, o las 00:01:00 UTC del primer día de cada mes. 

La forma en que se genera esta validación de la hora debería ser menos propensa a errores para el renovador, y más fácil para el retador para detectar un error. Una solución que podría evitar las cadenas de caracteres largas es acortar el hash en un hash aún más corto a través de algún algoritmo de acortamiento. Lo ideal sería que consistiera en 4-6 caracteres


