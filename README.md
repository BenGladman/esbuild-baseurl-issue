esbuild is erroneously resolving relative imports from baseURL. In the reproduction, `app.ts` outght to import `hello.ts`, not `hello.json`

The outputs from esbuild and tsc are included in this repo.

`node ts/dist-esbuild/app.js` prints `{ message: 'I AM JSON' }`

But `node ts/dist-tsc/app/app.js` prints `I AM TYPESCRIPT`
