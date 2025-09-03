---
title: 'Aaron Patterson sobre los revolucionarios del código abierto'
date: 2021-10-14
draft: false
summary: 'Aaron Patterson conversa con julia y amanda sobre instalar Linux por primera vez, la historia detrás de su primer parche, las dudas iniciales sobre el forking, y comparte algunos consejos para otros programadores. Incluye muchos malos juegos de palabras de todos.'
storyteller: 'Aaron Patterson'
storycorps: '85873752'
bio: 'Aaron Patterson es Senior Staff Engineer en Shopify, donde se centra en el desarrollo del núcleo de Ruby y Rails. Además de sus logros en software (numerosos y significativos), es conocido por su humildad, amabilidad y sus incursiones creativas en la escritura humorística.'
facilitators: ['julia ferraioli', 'amanda casari']
story_audio: 'https://media.blubrry.com/1466155/content.blubrry.com/1466155/Aaron_Patterson_on_open_source_game_changers.mp3'
explicit: 'no'
bytes: 38309764
tags:
  - GitHub
  - GPL
  - Ruby
---

**julia ferraioli**: Hola, me llamo julia ferraioli. Hoy es 14 de octubre de 2021. El tiempo ya no tiene sentido. Lo siento. Estoy aquí con amanda casari y Aaron Patterson. Aaron es nuestro narrador de hoy. Estoy grabando esta conversación para _Open Source Stories_ desde mi oficina en Seattle, Washington, donde curiosamente hace sol en este momento, lo cual es muy raro. Voy a pasarle la palabra a amanda para que se presente.

**amanda casari**: Hola, me llamo amanda casari. Estoy hablando con julia ferraioli y Aaron Patterson. Estoy grabando esta conversación para _Open Source Stories_. Siempre seguimos este mismo guion; puede sonar repetitivo, pero está bien. El entorno en el que grabo ahora mismo es esa temporada espeluznante de Nueva Inglaterra, justo antes de Halloween, cuando las hojas ya alcanzaron su punto máximo y empiezan a caer. Anochece temprano. Me di cuenta de que necesitaba instalarme tarde y fue una experiencia realmente inquietante. Pero estoy emocionada de hablar con todos hoy.

**julia ferraioli**: Aaron, ¿quieres contarnos un poco sobre ti?

**Aaron Patterson**: Claro. ¿Es mi turno? Mi nombre es… perdón, voy a intentar decirlo con mi mejor voz de Ira Glass.

**julia ferraioli**: Perfecto.

**Aaron Patterson**: Es broma. No puedo hacerlo. Mi nombre es Aaron Patterson, y aquí estoy. ¿Desde dónde hablo? ¿Cómo va esto? ¿Debo decir mi nombre, la fecha y desde dónde hablo? Bien.

**julia ferraioli**: Puedes simplemente decir desde dónde hablas — eso basta.

**Aaron Patterson**: Mi nombre es Aaron Patterson. Hoy es 14 de octubre de 2021. Estoy hablando desde mi oficina en mi casa en Seattle, Washington. Y sí, puedo confirmar que afuera hay un poco de sol ahora mismo. Sí.

**julia ferraioli**: Muy extraño. Bueno, gracias por acompañarnos hoy. Creo que te conocí por primera vez en un meetup de Ruby aquí en Seattle. Fue hace bastante tiempo.

**Aaron Patterson**: Sí, así fue. Estaba tratando de recordar — ¿dónde nos conocimos por primera vez? Y no podía, porque vivíamos en el mismo vecindario. Así que te veía todo el tiempo. Entonces pensé: "Oh, claro, ¿dónde fue que la conocí por primera vez?" Seguro fue en un meetup de Seattle Ruby.

**julia ferraioli**: Sí, yo era una completa novata — todavía lo soy, para ser honesta.

Me preguntaba si podías darme una idea de tu primera experiencia con la tecnología.

## Códigos secretos y subversión de sistemas

**Aaron Patterson**: Vaya… La tecnología ha estado a mi alrededor prácticamente toda mi vida. Mi madre es ingeniera eléctrica. Así que cuando crecía, siempre teníamos aparatos electrónicos en casa. Mi padre también es ingeniero. Y aprendí mucho de ambos. De hecho, cuando era niño me fascinaban los códigos secretos. Quería escribir código, enviar mensajes secretos a mis amigos, ¿no? Mi madre me enseñó binario. Ella me dijo: "Puedes usar esto. Codifica tu mensaje en unos y ceros, y luego dáselo a tus amigos". Yo pensé: "¡Increíble! ¡Fantástico!".

Me parecía increíble, pero convencer a mis amigos en la escuela no funcionaba. Ningún estudiante de tercer grado iba a codificar mensajes en unos y ceros para pasarse notas en clase. Pero sí, la tecnología siempre ha estado a mi alrededor.

**julia ferraioli**: Recuerdo haber aprendido sobre diferentes bases cuando era niña también. Creo que tuve una crisis existencial en ese momento. Así que felicitaciones por no tener una crisis existencial.

**Aaron Patterson**: No recuerdo exactamente cómo surgió, pero ella simplemente me dijo "okay, sabes, puedes hacer todo esto con unos y ceros". Y yo "¡¿quééé?!"

**amanda casari**: Esto me da mucha esperanza porque no tuve ese tipo de exposición cuando era niña, a la tecnología, aunque mis padres — mi madre hacía química y mi padre era ingeniero naval. No tuve nada de eso. Pero hago ese tipo de cosas con mis hijos. Como "oh, ¿preguntas cómo funciona esto? Sentémonos y hablemos de ello". Y mi hijo mayor, que ahora tiene 10 años, me dice cosas como "sí, pero no una gran explicación, mamá".

**julia ferraioli**: Buen establecimiento de límites.

**Aaron Patterson**: Solo tienes que convertirlo en código de alguna manera. Como, ¿cómo pueden disfrutar la tecnología o usarla con sus amigos? Usarla para subvertir sistemas.

**amanda casari**: Creo que tuvimos una buena base con Harriet la Espía, donde algunas cosas, aunque el escenario era de hace más tiempo, pero mucho de ese deseo de ser Harriet la Espía tenía algunas ramificaciones interesantes.

**Aaron Patterson**: Déjame enseñarte un truco: clic derecho -> Ver código fuente [sonidos de explosión].

**julia ferraioli**: Okay, soy muy consciente de mis habilidades de gestión del tiempo aquí. Ahora, Aaron, eres bastante activo en la comunidad de código abierto... ¿Cuál fue tu primer encuentro con ello? ¿Cómo te involucraste?

## Instalando Linux, ansiedad con `xf86config`, y el primer parche

**Aaron Patterson**: Supongo que mi primer encuentro como usuario probablemente fue cuando estaba en la preparatoria, instalé Linux en la computadora de mis padres y creo que es la primera vez que recuerdo haber tenido sudores fríos de verdad. Porque era como "Oh, ¿qué pasa si no puedo recuperar Windows en esta cosa? ¿Qué pasa si he arruinado permanentemente esto?"

Cuando estaba configurando Linux, había esta cosa como, en ese entonces tenías que hacer esto para configurar X windows, hacías `xf86config`. Y leía toda la documentación. Y había esta cosa, era como, okay, tienes que configurar la frecuencia para el monitor... como alguna configuración para la tarjeta de video o monitor o algo. Y había esta gran advertencia que decía como, si haces esto mal, literalmente puedes freír la computadora. La va a _freír_. Y yo "oh, hombre, ¡espero no arruinar esto!" De alguna manera lo logré.

Pero estaba tomando clases de programación en la preparatoria. En clase, usábamos el compilador Borland C, y no quería pagar por eso. Así que estaba instalando Linux para obtener un compilador C.

Pude recuperar Windows ahí. Así que estaba bien, pero vaya, estaba realmente nervioso.

**julia ferraioli**: ¿Un poco tenso?

**Aaron Patterson**: Sí, sí, seguro.

Como contribuidor, creo que hice mi primera contribución en — lo recuerdo en 2001. Era programador de Perl en ese momento. Trabajaba para una empresa llamada classmates.com. Que puede que conozcas o no... algunas personas mayores pueden recordar... Teníamos un sistema donde y — sé que esto está mal, pero acéptenlo tal como es. Almacenábamos a todos en el sistema. Para quienes no lo sepan, este sitio web era básicamente como un directorio escolar. Te registrabas y podías ver a todas las personas que se graduaron el mismo año que tú, y podías contactar a la gente. Es básicamente como un registro de graduados escolares. Almacenábamos el nombre de todos en mayúsculas. Ingresabas tu nombre, y no importaba lo que ingresaras, simplemente lo poníamos en mayúsculas y lo metíamos en la base de datos.

Recuerdo que la razón en ese momento era porque Oracle podía hacer búsqueda de texto en mayúsculas — si todo estaba en el mismo caso, podía hacer búsqueda de texto más rápido. Así que hacían eso. Pero por supuesto, cuando veías el directorio, nadie quería ver su nombre en mayúsculas, ¿verdad? Así que por supuesto la mejor solución para esto era, teníamos una biblioteca de Perl que tomaba las mayúsculas y trataba de adivinar el caso, trataba de ponerlo correctamente cuando se mostraba al usuario.

El problema era — funcionaba bastante bien, funcionaba okay con la mayoría de nombres estadounidenses. Pero luego empezamos a tener muchos latinoamericanos registrándose y no funcionaba para ellos en absoluto. Así que mi primera contribución de código abierto fue un parche a esta biblioteca que le daba un modo español. Así que podías decir "okay, ahora queremos ajustar esto para modo español".

Y creo que esa fue mi primera contribución de código abierto.

**amanda casari**: ¿Puedo preguntar — recuerdas cómo obtuviste la distribución de Linux que instalaste por primera vez?

**Aaron Patterson**: Oh, sí. CD en un libro en Barnes and Noble.

**amanda casari**: ¿Y cómo contribuiste el primer parche? ¿Enviaste un CD en un libro?

**Aaron Patterson**: No, no, no, no. Había listas de correo. Tenía que hacer un parche, y luego enviarlo a una lista de correo. Pero no había GitHub ni nada. No podía encontrar un repositorio para esto en absoluto. Básicamente tenía que parchearlo y hacer un diff y luego enviar por email un diff al autor y decir "hey, ¿puedes agregar esto?" Y luego lo hicieron.

**julia ferraioli**: ¿Recuerdas algún comentario de revisión que recibiste para ese parche?

**Aaron Patterson**: Oh, cero. Así que solo le envié un email al autor con un parche. Y dije "Hey, estamos usando esto en el trabajo. Y necesitamos un modo español. No maneja estos casos." Como les di una lista de nombres. Dije "no maneja estos casos, no maneja estos casos." El autor básicamente dijo "Oh, está bien. Hecho."

**julia ferraioli**: Muy relajado.

**Aaron Patterson**: Sí, fue un proceso bastante fácil. Pero diría que esa fue mi primera contribución de código abierto, y probablemente fueron muchos años después de eso antes de que hiciera muchas más contribuciones de código abierto.

**julia ferraioli**: ¿Sientes que eso tejió el código que realmente te hizo _tú_? ¿Tu contribución a Perl?

**Aaron Patterson**: No.

**julia ferraioli**: El peor juego de palabras de todos los tiempos.

**amanda casari**: Forzado. Fue un muy buen estiramiento. Creo que se te cayó algo ahí, tal vez.

**julia ferraioli**: Solo estoy tratando de hilar una historia.

**Aaron Patterson**: [Susurro] Okay.

**julia ferraioli**: Me disculpo.

**Aaron Patterson**: Está bien. Está bien. Quiero decir, esto pasa en muchos casos. Hay que hacer el cambio.

**julia ferraioli**: Bueno, en esa línea, cambiemos un poco. Sé que te enviamos algunas preguntas para hoy. ¿De qué te gustaría hablar?

**Aaron Patterson**: Oh, hombre, esa era como la única pregunta. "¿De qué quieres hablar?" Podemos hablar de cualquier cosa. Podemos hablar de hacer queso. Podemos hablar de hacer queso. Pero sé que esto es algo de código abierto. Así que podemos hablar de otras cosas también. No sé. Es una pregunta tan abierta. No tengo idea.

**julia ferraioli**: Pero reduzcámoslo un poco. Una de las cosas que estamos explorando son momentos pivotales en el código abierto o la evolución de los contribuidores de código abierto. ¿Hay un momento que tú o la industria hayan experimentado algo así que te gustaría compartir?

**Aaron Patterson**: SÍ.

## La GPL

**Aaron Patterson**: Leí esta pregunta, y me gustó. Supongo que he estado programando profesionalmente desde 1999. Así que he estado programando por mucho tiempo e involucrado en la comunidad de código abierto por mucho tiempo también. Así que he visto varios... no hay solo un pivote para mí, ¿verdad? Primero, creo, si le preguntas a cualquier desarrollador de código abierto esta pregunta, por supuesto, van a decir GPL. Tienen que, tienes que decir ese, porque fue importante. Porque antes de eso si no hubiéramos hecho eso, probablemente no tendríamos código abierto más, o no habríamos tenido código abierto en primer lugar.

Así que creo que ese fue un momento pivotal. Aunque creo que soy demasiado joven para saber... no soy lo suficientemente viejo para haber estado antes y después de la GPL. Como estuve después de la GPL. Pero creo que eso es lo que realmente impulsó el código abierto hacia adelante. Para mí, sin embargo. Creo que estamos viendo — bueno, ya lo hemos visto.

Hay otros dos puntos que quería hacer después de esto. Creo que ahora estamos viendo un movimiento para alejarse de la GPL. Así que no es realmente algo pivotal. Es más como un trasfondo. No hay un momento único, no sé cómo describir esto exactamente, ha habido un movimiento lento en la industria para alejarse de la GPL.

## La era GitHub, listas de correo, y el forking

**Aaron Patterson**: Y eso se relaciona con probablemente el punto pivotal más grande para mí en mi generación de programación, que probablemente sería GitHub. Solo porque contribuir a proyectos era tan difícil antes de que GitHub existiera; tenías que saber todas estas cosas. Tenías que ser capaz de descifrar como, okay, ¿quién es la persona correcta a quien enviar email? ¿Cómo armo un diff para esto, y luego envío un email a esa persona? Es solo que la barrera de entrada era tan alta que, para mí, GitHub fue realmente un momento pivotal para el código abierto. Y no estoy seguro de cómo se relaciona eso con lo de las licencias, pero sé que hay dos cosas pasando ahí.

**amanda casari**: ¿Recuerdas cuándo los proyectos en los que más estabas interesado y/o a los que contribuías se mudaron a GitHub?

**Aaron Patterson**: Rails es probablemente el más grande. Antes estábamos usando subversion en nuestro propio servidor alojado, creo que teníamos nuestro propio servidor alojado. Y luego movimos eso a GitHub, y fue importante. Fue súper agradable; alejarse de tu propio servidor alojado es simplemente, simplemente genial [risas]. Pero además de eso, con las otras cosas, como pull requests, eso no existía.

También recuerdo una cosa, cuando GitHub llegó, dijeron "haces fork de un proyecto", y en ese momento, yo estaba como "Whoa, puedes hacer fork de un proyecto. No puedes hacer eso. Eso no es legal." [Más risas.] Porque antes de esto hacer fork de un proyecto era importante. Si hacías fork del proyecto de alguien eso significaba que eras como "No, ustedes son los peores. Nunca voy a trabajar con ustedes otra vez. ¡Estoy haciendo fork de su proyecto!" Y ahora GitHub llega y como "No, solo haces fork. Haces tus cambios, y simplemente lo envías de vuelta..."

**julia ferraioli**: Siento que todavía está el fork minúscula y el Fork mayúscula.

**Aaron Patterson**: Creo. Creo que en mi mente, antes de GitHub, no había fork minúscula. Solo había parches, solo enviar parches, ¿verdad? No había fork minúscula. Solo hacer tu trabajo. Enviar un parche en algún lugar. Y luego GitHub nos dio el minúscula. Ahora puedes hacerlo. Ahora puedes hacer un fork grande.

**julia ferraioli**: Es el tenedor de cena versus el tenedor de ensalada.

**Aaron Patterson**: Exactamente, sí.

**amanda casari**: Es como sabes si estás en el lugar bueno o el lugar malo.

**Aaron Patterson**: El problema es que nunca sé qué tenedor usar. Así que como, ¿qué pasa si accidentalmente uso el tenedor grande?

**julia ferraioli**: Estoy segura de que la comunidad te lo dirá.

**amanda casari**: ¿Se sintió un poco grosero la primera vez que hiciste el fork?

**Aaron Patterson**: Oh, no, no, no lo fue. Una vez que alguien me explicó el flujo de trabajo, yo estaba como "Okay. Sí, está bien. Está bien. Es solo una palabra. Está okay." Pero sí recuerdo pensar como "oh, hombre, ¿está bien hacer esto?"

**julia ferraioli**: Cuando GitHub se lanzó por primera vez, en realidad no estaban enfocados en código abierto. ¿Verdad? ¿Plataforma de codificación social?

**Aaron Patterson**: Creo que eso es cierto. Solo eran una plataforma de codificación social. Pero quiero decir, no sé qué más serías. Si va a ser social, tiene que ser código abierto, básicamente. ¿Verdad? Especialmente si solo estás lanzando un sitio web, ¿quién más lo va a usar? No puedes codificar socialmente tu proyecto de código cerrado. Como, ¿cómo es eso social?

**julia ferraioli**: ¿Tu plataforma de codificación antisocial?

**Aaron Patterson**: Sí.

**julia ferraioli**: Es cierto. Pero el advenimiento de esta plataforma amigable al usuario que hizo que no tuvieras que enviar por email al autor de la biblioteca un parche, porque no sabes dónde está el repositorio, eso fue un cambio enorme para el código abierto, y la industria del código abierto.

**Aaron Patterson**: Antes de eso teníamos SourceForge, que era algo así, pero no ofrecían... La oferta principal de GitHub era un pull request, como esa era **_la_** cosa. No podías hacer eso en SourceForge. Tenían alojamiento, pero aún tenías que enviar por email un parche en algún lugar. Y también, en ese momento, SourceForge estaba tratando de monetizar. Así que se llenaron de anuncios. No sé si esto es apropiado para esto.

**julia ferraioli**: Mi primera experiencia con código abierto fue en SourceForge. Y tenías que ser muy cuidadoso dónde hacías clic.

**Aaron Patterson**: Recuerdas — tenían botones de descarga, que eran descargas totalmente falsas. Eran básicamente anuncios o algo como "¿cómo es esto, cómo es esto legal? Esto realmente se siente como un cebo y cambio como no deberías hacer esto." Así que creo que eso le dio a GitHub una gran ventaja porque era como "oh, hey, este sitio web no tiene anuncios por todas partes."

**amanda casari**: Así que tengo curiosidad Aaron, cuando los proyectos empezaron a moverse a GitHub, si ya no estabas enviando parches por email a la gente, ¿las listas de correo seguían siendo tan activas o tan ricas para conversación como eran antes? ¿O habían cambiado?

**Aaron Patterson**: Esa es una muy buena pregunta. Creo que básicamente han disminuido con el tiempo. Quiero decir, cuando GitHub se lanzó por primera vez, sí, por supuesto, las listas de correo seguían funcionando y todo eso enviabas emails a mucha gente y era divertido. En realidad, listas de correo e IRC — eso es algo que recuerdo con cariño; eso era muy divertido. Pero esas cosas son tan difíciles de usar que siento que son menos inclusivas, si eso tiene sentido. Pero sí, creo que la actividad de las listas de correo definitivamente ha disminuido con el tiempo. Quiero decir, solía estar en la lista de correo de Ruby. No estoy. No he leído la lista de correo por mucho tiempo [risas]. Odio admitir eso pero...

**julia ferraioli**: Lo escucharon aquí, gente.

**Aaron Patterson**: Sí, leo la lista de correo ruby-core, pero no realmente. Así que la lista de correo ruby-core es básicamente solo un espejo de nuestro sitio web. Como el sitio web de seguimiento de issues. Solo leo el sitio web de seguimiento de issues. No me gusta el email. Recibo demasiado email, si miras mi teléfono, dice que tengo más de 10,000 emails sin leer. Y miro eso, y estoy como "veamos si podemos llegar a 11,000." [Risas.]

**julia ferraioli**: Suena como mis notificaciones de GitHub.

**Aaron Patterson**: Oh, sí. Me rendí con eso hace mucho tiempo. El próximo GitHub será GitHub, pero sin notificaciones.

**julia ferraioli**: ¿Así que qué otros tipos de cambios viste con el advenimiento y la adopción de GitHub?

**Aaron Patterson**: No sé. Quiero decir, más CI, CI no existía. Mucha gente trató de hacer CI, pero nadie podía hacerla rentable. Supongo que hasta que Travis llegó, creo que fueron la primera empresa exitosa en hacer CI y realmente sobrevivir. Había habido un montón de otras empresas antes de eso que recuerdo que tenían ofertas de integración continua, pero todas quebraron. Así que sí, está eso.

¿Otras cosas que cambiaron? No sé. IRC muriendo. Ahora, en lugar de usar IRC, podemos usar Slack. Y es básicamente como IRC excepto que es lento y usa toda tu memoria. Supongo que sabes de qué deberíamos hablar, deberíamos hablar de editores. Porque eso es algo que ha cambiado enormemente con el tiempo. Creo, sin embargo, que soy una persona triste. He estado usando vim por 20 años.

**amanda casari**: Creo que ese es el tiempo que julia ha estado atrapada en él. Así que realmente apreciaría una salida.

**Aaron Patterson**: Vim, no puedo dejarte.

**julia ferraioli**: Bueno, en realidad, estoy en vim. Pero es vim dentro de Emacs. En realidad ya no sé dónde estoy. Eliza me está ayudando a salir.

**Aaron Patterson**: ¿Cuál es esa película donde siguen yendo más profundo? Esto es Inception. vim, Emacs, Inception.

**amanda casari**: Sí. Inception de editores.

**julia ferraioli**: Pero los editores más amigables al usuario, especialmente con varias integraciones? Revolucionario.

## La revolución de los editores

**Aaron Patterson**: Seguro. Creo que una de las mejores cosas que han salido recientemente, en mi opinión, es VSCode. Creo que es increíble. No lo uso, pero creo que es realmente asombroso para la comunidad de desarrollo, y la comunidad de código abierto en general, ¿verdad? Admitiré, vim no es fácil de usar. No es fácil de usar, pero ese es el que uso. Y ese es con el que quiero quedarme. Pero que alguien saliera y desarrollara un editor que la gente nueva puede usar y acostumbrarse e involucrarse en programación. Es importante para mí. Creo que es realmente, realmente increíble.

**amanda casari**: Creo que es interesante también, especialmente escuchando sobre tu experiencia con tu primera instalación de código abierto, y lo aterrador que era pensar "¿Qué pasa si destruyo la tecnología que en realidad estoy tratando de cambiar o con la que trabajar?". Pero tantas herramientas, especialmente en los últimos años ahora tienen esa capacidad de tener interoperabilidad, e integración, y poder construir estas cadenas y flujos de trabajo, con buena documentación. Así que no es este proceso místico se siente realmente revolucionario. Cambia mucho poder hacer cosas sin necesariamente tener que tener a alguien que no puede abordarlo desde el principio o ser nuevo en la comunidad o venir y hacer buenas preguntas educadas buscando cosas sobre cómo contribuir pero no tiene que aprender un código secreto?

**Aaron Patterson**: Absolutamente. Estoy totalmente de acuerdo. Es tan bueno, tener estas herramientas que son fáciles de usar. Supongo que soy un gran fanático de las cosas que bajan la barrera de entrada. Así que GitHub es una de esas cosas y estos nuevos editores, esa es otra cosa. Y creo que solo va a mejorar. No tengo idea de cómo, como, no puedo imaginar. No sé cómo vamos a bajar más la barrera. Pero creo que seguiremos bajándola. Y creo que eso es algo bueno.

**julia ferraioli**: Increíble. Gracias, Aaron. Solo tenemos 10 minutos restantes. Sé que estabas preocupado por la duración. Así que acabamos de cubrir predicciones, o la falta de ellas tal vez. ¿Dónde ves algunos de los problemas no resueltos en código abierto? ¿Los desafíos?

**Aaron Patterson**: Leí esta pregunta. No sé; es difícil. Es difícil de decir. Una de las cosas que escribí es, bueno **_la cosa_** que escribí es la sostenibilidad del código abierto. Porque mucha gente hace código abierto en su tiempo libre, y no creo que eso sea realmente sostenible. Cuando empecé a hacer código abierto... En 2001, tenía 21 años. Supongo que tenía 20. No estaba casado, podía simplemente hacer sabes, tenía mucho tiempo libre. Y mucha gente no tiene ese lujo. Así que creo que ese es un desafío realmente grande del código abierto es ¿cómo podemos darle a la gente ese tiempo para ponerlo en ello? Realmente no tengo buenas soluciones para eso. Cada avenida que he investigado para esto tiene algún tipo de problemas. Así que no sé. Pero creo que ese es un desafío. Y si podemos romper esa nuez, creo que ayudará mucho.

**julia ferraioli**: Definitivamente es un problema no resuelto. Creo que mucha gente tiene varios pensamientos. Y, sí, no creo que tengamos una solución que aborde todas las preocupaciones.

**Aaron Patterson**: No, quiero decir, hay varios — ahora mismo mi trabajo diario es que hago código abierto. Me tomó muchos, muchos años, pero finalmente encontré una empresa que es como "Sí, te pagaremos para hacer programación de código abierto". Pero no todos pueden hacer eso. Así que ¿qué más? ¿Cómo hacemos que paguen a la gente de otra manera? ¿O cómo les damos tiempo libre a las personas? Sí, no tengo una buena respuesta. Es un tema difícil.

**julia ferraioli**: Todos somos bastante privilegiados, en esta conversación de tener código abierto como parte de nuestros trabajos. Pero definitivamente no es así para todos. Y sé que uno de los problemas que vemos es que cada vez más tu currículum de código abierto está siendo considerado como un componente de contratación. [Gemidos.]

**Aaron Patterson**: Sí, eso me mata.

**amanda casari**: Es el mes perfecto para hablar de eso también.

**Aaron Patterson**: Realmente no me gusta cuando la gente usa código abierto como currículum. Quiero decir, algunos de los mejores programadores que conozco, no hacen código abierto, pero son realmente geniales. Son realmente geniales. Son buenos ingenieros. Así que sabes, ¿por qué? ¿Por qué necesitamos esto?

**amanda casari**: Así que tengo una pregunta para ambos entonces. He visto código abierto como una gran manera de tener un currículum público es como uno de los incentivos que he visto para gente que busca entrar en tecnología o busca ser contratada por ciertas empresas o posiciones. Así que siento que a veces se vende de esa manera para la gente porque hay una idea de que tiene una ventaja y tal vez la tiene incluso para hacer una primera contribución, es como "oh, haz una primera contribución. Ahora tienes un currículum público, la gente ve que entiendes las herramientas". ¿Sienten que... ¿eso surgió porque resolvía un problema antes? ¿O antes? ¿Fue en algún momento algo que realmente resolvía el problema que existía antes que simplemente ya no existe ahora? ¿O encontramos que era una mala práctica porque era tan excluyente?

**Aaron Patterson**: Esa es una muy buena pregunta. Así que para darte un poco de contexto sobre mí de mi experiencia. Una de sus preguntas era "¿qué lamentas?"

**julia ferraioli**: Agradable y ligero.

**Aaron Patterson**: Sí. Muy ligero. Una de las cosas... una razón por la que empecé a contribuir al código abierto es que uno de mis arrepentimientos es que no terminé la universidad. Así que cuando la gente está tratando de, o cuando estás buscando trabajo? Quiero decir, quiero ser programador. Pero ¿cómo puedes probar a empleadores potenciales que eso es algo que realmente puedes hacer? Y el código abierto es una manera de probar eso. Es como "bueno, no tengo experiencia laboral, pero puedes ver que hice XYZ". Y quiero decir, no sé. Creo que es una buena manera de demostrar que tienes las habilidades incluso si no tienes el historial laboral, pero admito, en ese momento, tenía mucho tiempo libre, así que pude hacer eso.

**julia ferraioli**: Así que voy a tomar la salida fácil y culpar al hecho de que solo tenemos unos minutos restantes para pasar la pregunta, y preguntarte, Aaron, ¿tienes algún pensamiento final para la gente que escucha o lee?

**Aaron Patterson**: ¿Pensamientos finales? Vaya, puedo simplemente bajar por toda la lista de cosas — leí todas las preguntas, y respondí todas las preguntas. ¿Debería simplemente ir? Voy a pasar por cada una de ellas. No hice pensamientos finales sin embargo, así que no sé.

## Pensamientos finales

**Aaron Patterson**: Tengo un buen pensamiento final para ustedes: El océano. [Pausa, luego risas.] No, No, No, estoy bromeando. Estoy bromeando. Así que esto es solo una broma. Supongo que tengo muchos pensamientos finales. Una cosa. Dios, no puedo elegir, es tan difícil para mí elegir solo uno. Así que tal vez voy a enumerar algunos.

Uno volviendo a lo del editor. Consejo que me gustaría dar a gente que son programadores, gente que quiere ser programador, o son programadores es no importa qué editor uses, pero apréndelo bien. Aprende cómo usar bien el editor. La razón por la que digo eso es porque de mi experiencia he usado vim más tiempo del que he usado cualquier lenguaje de programación. Y puedo hacer cualquier lenguaje de programación en ese editor. Así que para mí la cosa que es probablemente la pieza de tecnología más importante en mi computadora es ese editor, así que cualquiera que uses, apréndelo. Creo que se nos está acabando el tiempo aquí... un pensamiento final... como algo profundo...

**julia ferraioli**: Bueno, creo que un buen pensamiento final es agradecerte por acompañarnos hoy.

**Aaron Patterson**: Sí, mi otro pensamiento final es mi cabello. [Silencio]

**julia ferraioli**: Esto ha sido un deleite absoluto. Gracias.

**Aaron Patterson**: Gracias, me divertí.

**julia ferraioli**: Y espero que podamos tenerte de vuelta en algún momento pronto.

**Aaron Patterson**: Yo también. Me encantaría, gracias.

**julia ferraioli**: Gracias _a ti_.

**Aaron Patterson**: ....y, corte.