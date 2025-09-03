---
title: "El viaje de Russell Keith-Magee hacia el código abierto"
date: 2021-10-05T19:07:35-07:00
draft: false
summary: "Russell Keith-Magee se conecta con Open Source Stories para hablar sobre sus primeros recuerdos de tecnología, relatar cómo se involucró con el ecosistema Django, y compartir sus pensamientos sobre el contractualismo de código abierto."
storyteller: "Russell Keith-Magee"
storycorps: "85873751"
bio: "El Dr. Russell Keith-Magee es el fundador del proyecto BeeWare, desarrollando herramientas y bibliotecas GUI para apoyar el desarrollo de software Python en plataformas de escritorio y móviles. También ha sido miembro del equipo central de Django desde 2006, y durante 5 años, fue Presidente de la Django Software Foundation. En su trabajo diario, maneja pipelines de datos para Upwave. Es un orador frecuente en conferencias de Python y Django alrededor del mundo, compartiendo su conocimiento y experiencias como desarrollador FLOSS, mantenedor de comunidad, y fundador de startup (no exitoso)."
facilitators: ["amanda casari", "julia ferraioli"]
story_audio: "https://media.blubrry.com/1466155/content.blubrry.com/1466155/Russell_Keith-Magee_s_journey_to_open_source.mp3"
explicit: "no"
bytes: 37945722
tags:
- Python
- Compassion
- Django
- Community
---
**julia ferraioli**: Mi nombre es julia ferraioli, y mis pronombres son ella/ella. Hoy es 5 de octubre de 2021. Y estoy hablando con Russell Keith-Magee, quien es un tecnólogo comprometido, desarrollador principal en el proyecto Django, y el fundador del proyecto beware. Estoy grabando esta conversación para open source stories en una oficina bastante espartana que aún no he decorado después de mudarme. Y mi primer recuerdo de una computadora es en realidad jugar Wheel of Fortune en MS DOS, si pueden creerlo. Eso fue hace mucho tiempo. Y Russell, ¿te gustaría presentarte?

**Russell Keith-Magee**: Sí. Hola, mi nombre es Russell Keith-Magee. Estoy hablando hoy desde Perth, Australia Occidental, que es Whadjuk Nyoongar Boodja; los Whadjuk Noongar son los propietarios tradicionales de la tierra desde donde estoy grabando. Debido a las zonas horarias, en realidad es 6 de octubre donde estoy grabando -- ¿las zonas horarias cómo funcionan? Mi primer recuerdo de una computadora es en realidad mi padre trayendo a casa una Macintosh Apple original. Mi padre estaba muy interesado en experimentar con tecnología nueva y extravagante, así que teníamos una Commodore64 en la casa muy muy temprano.

Pero antes de eso, antes de que tuviéramos esa, él tuvo para una prueba durante un fin de semana una Macintosh original que trajo a casa y recuerdo vívidamente descubrir -- sin idea de qué iba a hacer con esta cosa -- pero descubrí que había un programa de pintura y podías dibujar y podías dibujar cosas con pintura. Pero si tenías el pincel más gordo, y coloreabas toda la pantalla completamente de negro, y luego hacías clic en reset, pasaría por un par de tonos de escala de grises mientras el color se desvanecía. No sé por qué eso me voló la mente que pudieras hacer eso. Está sentado en la oficina de mi padre viendo sus dedos afeitarse pasar por fases de gris divirtió al yo de siete años, supongo.

**julia ferraioli**: Me parece recordar efectos como esos yo misma, así como iniciar manualmente un protector de pantalla. Que por supuesto, si lo habías dejado funcionando demasiado tiempo, se quemaría en los monitores.

**Russell Keith-Magee**: Sí.

## Sobre la compasión

**julia ferraioli**: Así que gracias por acompañarme hoy. Estoy realmente emocionada de charlar contigo. Y quiero tener una pequeña idea sobre tu trasfondo. Profundicemos en las cosas realmente ligeras. Como... ¿cuáles son algunas lecciones importantes que has aprendido en tu vida?

**Russell Keith-Magee**: Supongo que ha sido una lección continua aprender que casi no hay situación donde tener compasión y empatía por las personas con las que estás tratando, eso no te servirá bien. En mi juventud, puedo recordar estar mucho más enojado y frustrado con todas estas otras personas estúpidas en el mundo que simplemente no entienden. A medida que he envejecido, he aprendido gradual y a veces muy dolorosamente que no es que todos los demás en el mundo sean estúpidos. Es solo que todos los demás en el mundo tienen un conjunto diferente de experiencias y un conjunto diferente de conocimientos y un conjunto diferente de antecedentes, un conjunto diferente de expectativas. Más a menudo que no, lo que se percibe como esta persona siendo estúpida, es solo que su conjunto de expectativas entrando en la situación son radicalmente diferentes a las tuyas. Sacarte de tu propia cabeza para ver de dónde vienen no solo hará que lidiar con el mundo sea mucho menos frustrante para ti, sino que a menudo puede ayudarte a llegar a cualquier objetivo compartido que estés tratando de alcanzar mucho más fácil.

Solo en virtud de que si entiendes de dónde viene alguien, es mucho más fácil presentar la información de una manera que van a poder entender o absorber o reconocer lo que sea que estés diciendo. Eso no es decir que no sea increíblemente frustrante a veces cuando aún estás en conversaciones, pero me ha ayudado a manejar mi frustración mucho más darme cuenta de dónde vienen otras personas o no vienen de un lugar de tratar activamente de frustrarme. Es solo un accidente del mundo siendo un lugar muy grande y complejo e intrigante.

**julia ferraioli**: Esa es una lección fantástica. A menudo tiendo a pensar en ello como que las personas están operando con diferentes variables de entorno establecidas.

**Russell Keith-Magee**: Sí, sí. Y hay muchas, muchas de ellas y no están documentadas en absoluto.

**julia ferraioli**: ¡No!

**Russell Keith-Magee**: Y muy a menudo ni siquiera están conscientes de las variables de entorno bajo las que están funcionando, lo cual es parte de la frustración, supongo. Pero sí, estar consciente de esas variables ambientales es útil.

## Primeras experiencias con código abierto

**julia ferraioli**: Excelente. Así que estás muy involucrado en el ecosistema de código abierto. Entonces, ¿cómo describirías el código abierto a alguien que no está familiarizado con él?

**Russell Keith-Magee**: Supongo que lo describiría como un proyecto colectivo donde un grupo de personas trabajan juntas para construir soluciones tecnológicas a un problema. Así que al compartir, no repiten el trabajo de cada uno. Y pueden aprender de las lecciones de cada uno. Si estás trabajando en un sistema por ti mismo, hay un límite a cuánto puedes hacer por ti mismo. Si incluso dos grupos pequeños están trabajando juntos, hay un límite a cuánto pueden lograr por su cuenta. Pero si todos están trabajando juntos y compartiendo juntos, terminas con una solución más robusta, más completa, porque tienes más input en lo que se está desarrollando y lo que se está construyendo.

Así que es, en algunos aspectos, la antítesis de lo que el capitalismo moderno está tratando de enseñarnos a todos a hacer, que sabes esa idea de que encuentras algo en lo que eres bueno y te aseguras de monopolizar el mercado para que nadie más pueda hacerlo. Es esta idea de que si todos contribuimos juntos, todos damos un poco hacia el proyecto. Todos avanzan un poco más como resultado.

**julia ferraioli**: Como este concepto de bien colectivo.

**Russell Keith-Magee**: Sí.

**julia ferraioli**: Entonces, ¿cuál fue tu primer encuentro con el código abierto? ¿Cómo te diste cuenta de él por primera vez?

**Russell Keith-Magee**: Me di cuenta del código abierto antes de que la palabra código abierto fuera siquiera una cosa, así que mi primera exposición fue a mediados de los 90. Estaba jugando con una computadora y alguien hizo el "Oye, oye, sabes, ¿has visto esta cosa llamada Linux?", y me pasó una gran pila de disquetes que podía instalar en mi computadora. Y hay todo este otro sistema operativo que era como completamente diferente de Windows. En ese momento, el software libre era una cosa. Y como usualmente haces, lees todo el código alrededor o la documentación y las declaraciones de manifiesto que están alrededor del software libre. Y esta era una idea fascinante de que esto es esta pieza de hardware, esta impresora era frustrante. Así que la gente liberó el software para ella para que pudieran programar su propia impresora como, sí, eso suena genial. ¿Cómo consigo más de eso?

Ese fue como el comienzo de mi carrera universitaria para cuando estaba, en mis años de honores, el movimiento de código abierto como lo entendemos ahora -- la OSI [[Open Source Initiative](https://opensource.org)] y grupos como ese -- estaban comenzando a formalizar lo que estaban diciendo, bajo una nueva narrativa sobre lo que eso significaría, que no estaba exactamente en los extremos de lo que la Free Software Foundation estaba empujando pero en una vena similar.

**julia ferraioli**: Entiendo. Hablaste sobre Linux, pero ¿hubo una primera pieza de software de código abierto que realmente te hizo comprar toda la cosa?

**Russell Keith-Magee**: Supongo que, si tuviera que poner mi dedo en ello, diría que probablemente fue el Escritorio GNOME, otra vez, en ese tipo de marco temporal de finales de los 90, cuando debería haber estado pasando mucho más tiempo trabajando en mi tesis, pero era solo estar intrigado por esta idea de un escritorio que podías construir y configurar y cambiar cosas