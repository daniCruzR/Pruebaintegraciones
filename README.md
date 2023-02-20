# Prueba Integraciones
Buen día, en el archivo index.html se encuentra el códgio con el cual se creó Kajita para la generación del token de la una suscripción bajo demanda. Se utilizó la documentación https://docs.kushki.com/pe/one-time-payments/card/on-demand, https://codepen.io/danicruzR/pen/jOvboxM. Con el token generado se realizaron las demás peticiones a través de la colección de Postman. En el archivo Subscription.postman_collection.json. se encuentran los request enviados. Se utilizó la documentación https://api-docs.kushkipagos.com/docs/online-payments/one-click-and-scheduled-payments para la creación de estos requests.
Merchant generado en uat: Integratest  Peru 20000000100140483000

Respuestas punto 4

• Experiencia de Onboarding con Kushki. Oportunidades de mejoras identificadas. 
R// El onboarding con Kushki siempre es destacado, comunican el estado de los procesos, regalan feedback para ambas partes mejorar, evaluan tu desempeño cada x periodo de tiempo, se preocupan porque sus colaboradores tengan o desarrolles las habilidades necesarias para el roll. 

• Experiencia con la documentación técnica. Oportunidades de mejoras identificadas y propuesta de mejora de esta. 
R// La docuementación técnica me pareció clara, gracias a ella pude realizar el punto 1. Tengo un comentario respecto a Kajita, en la documentación explican detalladamente como integrarla pero en el punto 1 de la prueba dice que la tokenización se puede realizar a través de kuskijs o Kajita. Por qué cuando es una suscripción bajo demanda desde kajita no se genera el token pero cuando es una suscripción calendarizada si? este comportamiento está ok?  adjunto evidencia https://codepen.io/danicruzR/pen/ZEMbZKz 

• ¿Qué entiendes por el concepto de tokenización y por qué cree que se recomienda  tokenizar por medio de una solución del frontend?. 
R// Se tokeniza una tarjeta para reemplazar cierta información del TH,luego de tener este campo se le realiza el cargo al cliente.
Se recomienda tokenizar por medio de una solución frontend para recolectar información del dispositivo en donde se realiza la transacción.

• Definir que es Autorización, Captura, Reversión, Anulación, Charge. 
R//
Autorización: es cuando se le toma cierto valor al TH en su TC para verificar que el cliente cuenta con suficiente crédito antes de procesar la venta.
Captura: En la captura se hace el cobro efectivo de la autorización y se le hace el débito al TH en su cuenta.
Reversión: Cuando se excede el tiempo de la anulación del cargo se procede con la reversión. Es un proceso Semi-automatio y en algunos casos se pueden realizar reembolsos parciales.
Anulación: Es la anulación de un cargo o un cargo diferido existoso. El TH tiene casi 72 hrs para realizar la anulación.
Cargo: Es cuando se le debita un monto al TH de su cuenta.

• Que entiendes y con qué fin se pueden utilizar llaves de idempotencia. 
Se usa para evitar duplicidad en las transacciones cuando se tiene una intermitencia en el flujo de pagos. Se envía en el header del HTTP, llega al receptor cuando se ejecuta el pago. Por ejemplo si existe una intermitencia y se le descuenta el dinero al usuario y se reintenta la transacción con la misma llave de idempotencia el receptor devuelve un mensaje indicando que ya se ha realizado el débito y no duplica el pago.


•¿Qué entiendes por el concepto de Webhook y cuál es su utilidad?
R// Un Webhook es un llamado que notifica cuando un evento ocurre, se usa para notificar a los usuarios eventos como por ejemplo el cobrro de una suscripción. 


5 
Para este punto se puden usar las colecciones de postman Subscription.postman_collection.json.
 y transfer Transfer In.postman_collection.json.
 
Los flujos ya se encuentran en la documentación, la cual es pública y puede tener acceso el comercio 
<img width="928" alt="image" src="https://user-images.githubusercontent.com/125845983/220162833-c114c6f9-80ba-40be-81c4-e4a3aa11738e.png">
https://docs.kushki.com/pe/one-time-payments/transfer/overview
<img width="754" alt="image" src="https://user-images.githubusercontent.com/125845983/220162902-3feda400-3b46-4a22-8790-fcfd172a8fcc.png">
https://docs.kushki.com/co/one-time-payments/card/on-demand

