# Alexa GeminiChat
### Modelo de Alexa Skill para integrar Google Gemini en dispositivos Alexa

**Visita el canal [Scintilla Hub](https://www.youtube.com/@scintillahub) en YouTube**

## Requisitos
*  Con una cuenta de Google, generar una clave de autenticación API en el sitio web de [Google AI Developer](https://ai.google.dev/). Copia y guarda la clave, sólo será visible cuando se cree.
* Crear una cuenta de [Amazon](https://www.amazon.com/ap/signin?openid.pape.preferred_auth_policies=Singlefactor&clientContext=132-2293245-7926858&openid.pape.max_auth_age=7200000&openid.return_to=https%3A%2F%2Fdeveloper.amazon.com%2Falexa%2Fconsole%2Fask&openid.identity=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.assoc_handle=amzn_dante_us&openid.mode=checkid_setup&marketPlaceId=ATVPDKIKX0DER&openid.claimed_id=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.ns=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0&) e iniciar sesión en la _Consola de Desarrollador de Alexa_.
## Crear una Alexa Skill
Crea una Alexa-hosted (Python) Skill en Alexa (_Create Skill_)

1. Name your Skill: Elige un nombre de tu elección (Ex: Chat GPT)
2. Choose a primary locale: Spanish (Spain)
3. Clik _Next_. En Tipo de habilidad selecciona: Other > Custom > _Alexa-hosted (Python)_
4. _Hosting region_: Puedes dejar la predeterminada _US East (N. Virginia)_ o Seleccionar _EU (Ireland)_
5.  En _Templates_: Clik _Import Skill_
6. Introduce la dirección del repositorio: https://github.com/jarios86/skill-alexa-geminiChat.git y acepta.

## Configurando la Skill
Cuando la importación se haya completado en _Invocations_ > _Skill Invocation Name_:
1. Editar _Skill Invocation Name_. Este será el comando de invocación para su skill. Si cumple con los requisitos y restricciones de palabras.
2. Clik en _Save_
3.  Cree la habilidad haciendo clic en _Build Skill_. Cuando termine, vaya a la pestaña **Code**
4.  Crea un archivo dentro de la carpeta Lambda llamado .env y añade la línea que añade la clave API generada:
   ```shell
   GOOGLE_API_KEY=TuClaveApiGoogleAI
   ```
5. Clik en _Save_ y luego en _Deploy_
   
## Prueba de la Skill
Una vez completado el _deploy_ ve a la pestaña **Test**:
1. En _Skill testing is enabled in_ cambia de _Off_ a _Development_
2. Para utilizar los comandos de voz acepte la solicitud del sitio para utilizar el micrófono, y para hablar haga clic y mantenga pulsado el icono del micrófono, y suelte para enviar.
3. Utiliza el comando de activación configurado para iniciar la Skill, ¡y ya estás listo para interactuar con Gemini a través de Alexa!

La Skill estará ahora disponible en todos los dispositivos Alexa vinculados a tu cuenta.
