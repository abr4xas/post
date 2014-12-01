Title: Evitando el spam con #reCAPTCHA
Date: 2012-02-29 06:13
Author:  
Slug: evitar-spam-recaptcha

![Logo
Recaptcha](http://abr4xas.org/wp-content/uploads/2012/02/457px-RecaptchaLogo.svg_.png "457px-RecaptchaLogo.svg")

reCAPTCHA es una extensión de la prueba CAPTCHA que se utiliza para
reconocer texto presente en imágenes. Emplea por tanto la prueba
desafío-respuesta utilizada en computación para determinar cuándo el
usuario es o no humano para, a su vez, mejorar la digitalización de
textos.

<span style="color: #ff0000;">[adsenseyu2]</span>

reCAPTCHA se basa en el hecho de que para un ser humano puede ser simple
determinar el texto presente en una imagen cuando para una máquina esta
tarea resulta en ocasiones demasiado compleja.[1]

<!--more-->Se llama spam, correo basura o mensaje basura a los mensajes
no solicitados, no deseados o de remitente no conocido (correo anónimo),
habitualmente de tipo publicitario, generalmente enviados en grandes
cantidades (incluso masivas) que perjudican de alguna o varias maneras
al receptor. La acción de enviar dichos mensajes se denomina spamming.
[2]

<span style="color: #ff0000;">[adsenseyu1]</span>

> *La palabra spam proviene de la segunda guerra mundial, cuando los
> familiares de los soldados en guerra les enviaban comida enlatada.
> Entre estas comidas enlatadas estaba una carne enlatada llamada spam,
> que en los Estados Unidos era y es muy común*. [2]

<span style="color: #ff0000;">[adsenseyu3]</span>

Al entender que es el reCAPTCHA y que es el SPAM hablemos ahora un poco
sobre como aplicar el reCAPTCHA en nuestro sitio:

Si usamos un CMS como:

-   Drupal: Existe un plugin para este sistema de administración de
    contenidos que lo pueden ubicar y bajar haciendo clic en este
    [enlace](http://drupal.org/project/captcha "reCAPTCHA para drupal ") y
    en este otro
    [enlace](http://www.cocinandocondrupal.net/node/70 "Instalar y configurar modulo anti-spam captcha").
-   Wordpress: Para este otro sistema de administración de contenidos
    existe un plugin (el que uso en este blog) en este
    [enlace](http://wordpress.org/extend/plugins/wp-recaptcha "WP-reCAPTCHA") pueden
    bajar el plugin y ahí obtener información de como instalarlo y como
    hacer la configuración.

<span style="color: #ff0000;">[adsenseyu4]</span>

Ahora bien, si tenemos un sistema propio lo que debemos hacer es lo
siguiente:

En el formulario de contacto o simplemente en el formulario de
comentarios debemos agregar lo siguiente:

-   Server Side

<!-- -->

     privatekey = "your_private_key";
      $resp = recaptcha_check_answer ($privatekey,
                                    $_SERVER["REMOTE_ADDR"],
                                    $_POST["recaptcha_challenge_field"],
                                    $_POST["recaptcha_response_field"]);

      if (!$resp->is_valid) {
        // What happens when the CAPTCHA was entered incorrectly
        die ("The reCAPTCHA wasn't entered correctly. Go back and try it again." .
             "(reCAPTCHA said: " . $resp->error . ")");
      } else {
        // Your code here to handle a successful verification
      }
      ?>

Esta es una información de ejemplo, para obtener mayor información de
como implementarlo
clic [aquí](http://code.google.com/apis/recaptcha/docs/php.html "Using reCAPTCHA with PHP").

Aplicando estos consejos pueden evitar el spam en sus sitios sin ningun
tipo de problema.

[**UPDATE**]  

` Habia olvidado comentarles que para la $privatekey y la $publickey deben estar registrados en http://www.google.com/recaptcha y luego de eso seguir las instrucciones que están aquí. Y bueno, eso es todo!!`  
[/**UPDATE**]  
@[xombra](http://twitter.com/xombra "Sigue a xombra en twitter!!"),
gracias por el dato!!

 

[1] [http://es.wikipedia.org/wiki/Recaptcha](http://es.wikipedia.org/wiki/Recaptcha "Recaptcha")

[2] [http://es.wikipedia.org/wiki/Spam](http://es.wikipedia.org/wiki/Spam "Spam")
