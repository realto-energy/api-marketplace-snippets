# Snippets to help integrate with the [re.alto energy API marketplace](https://portal.realto.io)

There's a wide variety of APIs available on [re.alto](https://portal.realto.io), each with it's own set of integration parameters. Follow the guidelines outlined within the specific API’s technical documentation regarding endpoints and parameters. 

In general all APIs will require a valid subscription and subscription token which is given once an API product has been sucessfully subscribed to. For authentication/authorisation all requests made to a specific API must include the subscription token in the header. The header key must be “Ocp-Apim-Subscription-Key” with the value being the subscription token itself. You can find your subscription token under the "My Subscriptions" area when logged in.

This repo was created to help get you up and running as quick as possible. Here you will find some boilerplate for a variety of coding languages which should help you query the APIs over the marketplace.
