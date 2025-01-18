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

## Configurando a Skill
Ao finalizar a importação em _Invocations_ > _Skill Invocation Name_:
1. Edite _Skill Invocation Name_. Este será o comando de invocação para sua skill. Se atende para os requisitos e restrições de palavras
2. Clique em _Save_
3. Realize o Build da Skill clicando em _Build Skill_. Ao finalizar, vá para a aba **Code**
4. Crie um arquivo dentro da pasta Lambda chamado _.env_ e adicione a linha, adicionando a API key gerada:
   ```shell
   GOOGLE_API_KEY=SuaApiKeyGoogleAI
   ```
5. Clique em _Save_ e então em _Deploy_
   
## Teste da Skill
Ao finalizar o _deploy_ vá para aba **Test**:
1. Em _Skill testing is enabled in_ mude de _Off_ para _Development_
2. Para usar comandos de voz aceite a requisição de uso do microfone pelo site, e para falar clique e segure o ícone de mic, e solte para enviar
3. Use comando de ativação configurado para iniciar a Skill, e pronto está interagindo com o Gemini pela Alexa!

A Skill já estará disponível em todos os dispositivos Alexa vinculados a sua conta.
