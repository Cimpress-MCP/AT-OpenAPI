# AT Squad OpenAPI Wrapper

A wrapper around Open API with logging and error handling.

## Using this library

Install the library.

```bash
yarn add @alphatango/openapi
```

```javascript
import { OpenApiWrapper } from '@alphatango/openapi';

const { api, getUserPrincipal, getRequestId, getUserToken } = new OpenApiWrapper(requestLogger);

api.get('/livecheck', () => {
  statusCode: 200;
});
api.any('/{proxy+}', () => {
  statusCode: 404;
});

export const lambdaHandler = api.handler;
```

## Contribution

We value your input as part of direct feedback to us, by filing issues, or preferably by directly contributing improvements:

1. Fork this repository
1. Create a branch
1. Contribute
1. Pull request
