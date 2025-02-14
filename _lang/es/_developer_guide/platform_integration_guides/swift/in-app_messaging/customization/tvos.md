---
nav_title: tvOS
article_title: Mensajes dentro de la aplicación para tvOS
platform: tvOS
page_type: reference
description: "Aprende a personalizar tus mensajes dentro de la aplicación para la plataforma tvOS de Apple."
page_order: 0
---

# Personalización de los mensajes dentro de la aplicación para tvOS

> Aprende a personalizar tus mensajes dentro de la aplicación para la plataforma tvOS de Apple.

{% alert important %}
Ten en cuenta que tendrás que implementar tu propia interfaz de usuario personalizada, ya que la mensajería dentro de la aplicación se admite a través de la interfaz de usuario sin cabeza mediante el SDK de Swift, que no incluye ninguna interfaz de usuario ni vistas predeterminadas para tvOS.
{% endalert %}

## Configuración de tu aplicación tvOS

### Paso 1: Crear una nueva aplicación iOS

En Braze, selecciona **Configuración** > **Configuración de la aplicación** y, a continuación, **Añadir aplicación**. Introduce un nombre para tu aplicación de tvOS, selecciona **iOS (no**_tvOS) y_luego selecciona **Añadir aplicación**.

![ALT_TEXT.]({% image_buster /assets/img/tvos.png %}){: style="width:70%"}

{% alert warning %}
Si seleccionas la casilla **tvOS**, no podrás personalizar los mensajes dentro de la aplicación para tvOS.
{% endalert %}

### Paso 2: Obtén la clave de API de tu aplicación

En la configuración de tu aplicación, selecciona tu nueva aplicación para tvOS y toma nota de la clave de API de tu aplicación. Utilizarás esta clave para configurar tu aplicación en Xcode.

![ALT_TEXT]({% image_buster /assets/img/tvos1.png %}){: style="width:70%"}

### Paso 3: Integrar BrazeKit

Utiliza la clave de API de tu aplicación para integrar el [SDK de Braze Swift](https://github.com/braze-inc/braze-swift-sdk) en tu proyecto de tvOS en Xcode. Solo tienes que integrar BrazeKit desde el SDK Swift de Braze.

### Paso 4: Crea tu interfaz de usuario personalizada

Como Braze no proporciona una interfaz predeterminada para los mensajes dentro de la aplicación en tvOS, tendrás que personalizarla tú mismo. Para un recorrido completo, consulta nuestro tutorial paso a paso: [Personaliza los mensajes dentro de la aplicación para tvOS](https://braze-inc.github.io/braze-swift-sdk/documentation/braze/in-app-message-customization). Para ver un proyecto de ejemplo, consulta [los ejemplos del SDK Swift de Braze](https://github.com/braze-inc/braze-swift-sdk/tree/main/Examples#inappmessages-custom-ui).
