`vc dev` Next.js error reproduction when using `getInitialProps()`.

```
TypeError: Cannot read properties of undefined (reading 'data')
    at executeBuild (/Users/chris/code/vercel/packages/cli/dist/index.js:233982:64)
    at processTicksAndRejections (node:internal/process/task_queues:96:5)
    at DevServer._start (/Users/chris/code/vercel/packages/cli/dist/index.js:235927:17)
    at dev (/Users/chris/code/vercel/packages/cli/dist/index.js:222558:5)
    at main (/Users/chris/code/vercel/packages/cli/dist/index.js:222658:16)
    at main (/Users/chris/code/vercel/packages/cli/dist/index.js:230261:24)
```

Error occurs on https://github.com/vercel/vercel/blob/main/packages/cli/src/util/dev/builder.ts#L312. `zipBuffer` 
does not exist.
