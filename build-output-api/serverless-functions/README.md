# Serverless Functions

## Build Output API

This Prebuilt Deployment example demonstrates how to output Vercel Serverless Functions using the [Build Output API](https://vercel.com/docs/build-output-api/v3#vercel-primitives/serverless-functions).

### Demo

https://build-output-api-serverless-functions.vercel.sh

### How it Works

In this case, the contents of the Serverless Function are located in the
[`.vercel/output/functions/index.func`](./.vercel/output/functions/index.func) directory.
This means that the Serverless Function will be accessible at the `/index` (or `/`) path of the Deployment.

The [`.vc-config.json`](./.vercel/output/functions/index.func/.vc-config.json) file specifies `"runtime": "nodejs14.x"`
which informs Vercel that the endpoint should be created as a Serverless Function, using Node.js version 14.

The `"handler": "index.js"` field indicates that the [`index.js`](.vercel/output/functions/index.func/index.js)
source code file will be the starting point of execution when the Serverless Function is invoked.

Additional files may placed within the `index.func` file as well which will be included in the runtime environment
of the Serverless Function. In this case, there is also a `node_modules` directory
that contains dependencies that the example Serverless Function needs in order to operate.
