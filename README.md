# Prueba Integraciones
Buen día, en el archivo index.html se encuentra el códgio con el cual se creó Kajita para la generación del token de la una suscripción bajo demanda. Se utilizó la documentación https://docs.kushki.com/pe/one-time-payments/card/on-demand, https://codepen.io/danicruzR/pen/jOvboxM. Con el token generado se realizaron las demás peticiones a través de la colección de Postman. En el archivo Subscription.postman_collection.json. se encuentran los request enviados. Se utilizó la documentación https://api-docs.kushkipagos.com/docs/online-payments/one-click-and-scheduled-payments para la creación de estos requests.
Merchant generaro en uat: Integratest  Peru 20000000100140483000

Respuestas punto 4

• Experiencia de Onboarding con Kushki. Oportunidades de mejoras identificadas. 
R// El onboarding con Kushki siempre es destacado, comunican el estado de los procesos, regalan feedback para ambas partes mejorar, evaluan tu desempeño cada x periodo de tiempo, se preocupan porque sus colaboradores tengan o desarrolles las habilidades necesarias para el roll. 

• Experiencia con la documentación técnica. Oportunidades de mejoras identificadas y propuesta de mejora de esta. 
R// La docuementación técnica me pareció clara, gracias a ella pude realizar el punto 1. Tengo un comentario respecto a Kajita, en la documentación explican detalladamente como integrarla pero en el punto 1 de la prueba dice que la tokenización se puede realizar a través de kuskijs o Kajita. Por qué cuando es una suscripción bajo demanda desde kajita no se genera el token pero cuando es una suscripción calendarizada si? este comportamiento está ok?  adjunto evidencia https://codepen.io/danicruzR/pen/ZEMbZKz 

• ¿Qué entiendes por el concepto de tokenización y por qué cree que se recomienda  tokenizar por medio de una solución del frontend?. 

• Definir que es Autorización, Captura, Reversión, Anulación, Charge. 

• Que entiendes y con qué fin se pueden utilizar llaves de idempotencia. 

•¿Qué entiendes por el concepto de Webhook y cuál es su utilidad?
R// Un Webhook es un llamado que notifica cuando un evento ocurre, se usa para notificar a los usuarios eventos como por ejemplo el cobrro de una suscripción. 
