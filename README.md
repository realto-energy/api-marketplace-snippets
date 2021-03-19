# Snippets to help integrate with the [re.alto energy API marketplace](https://portal.realto.io)

There's a wide variety of APIs available on [re.alto](https://portal.realto.io), each with it's own set of integration parameters. Follow the guidelines outlined within the specific API’s technical documentation regarding endpoints and parameters. 

In general all APIs will require a valid subscription and subscription token which is given once an API product has been sucessfully subscribed to. For authentication/authorisation all requests made to a specific API must include the subscription token in the header. The header key must be “Ocp-Apim-Subscription-Key” with the value being the subscription token itself. You can find your subscription token under the "My Subscriptions" area when logged in.

This repo was created to help get you up and running as quick as possible. Here you will find some boilerplate for a variety of coding languages which should help you query the APIs over the marketplace.

## Table of Contents

1. [Curl](#curl)
2. [Python](#python)
3. [JavaScript (Axios)](#axios)

<a name="curl"></a>
####  Curl

```
curl -v -X GET "https://api.realto.io/example/operation?key=value" -H "Cache-Control: no-cache" -H "OCP-Apim-Subscription-Key: YOUR_SUBSCRIPTION_KEY"
```
<a name="python"></a>
####  Python

```
# script.py

endpoint = '' # The API endpoint, e.g. https://api.realto.io/example/operation
token = '' # Your API subscription key
params = {'exampleKey': 'exampleValue'} # Any query params for the operation
response = requests.get(endpoint, headers={'OCP-Apim-Subscription-Key': token}, params=params)
json = response.json()
```
<a name="axios"></a>
####  JavaScript (Axios)

```
// example.js

import axios from 'axios'; // Alternatively const axios = require('axios') depending on your specific set-up
const BASE_URL = ''; // Base URL of request, e.g. https://api.realto.io/example
const headers = { 'OCP-Apim-Subscription-Key': 'Your API subscription key'}
const params = { exampleKey: 'exampleValue' }; // Any query parameters to include
const getRequest = async () => {
  try {
	const response = await axios.get(`${BASE_URL}/operation`, { headers, params });
	console.log(response);
	return response;
  } catch (errors) {
    console.error(errors);
  }
};
getRequest();
```
