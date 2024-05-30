# Overview

Reproduction for [this GitHub issue](https://github.com/sveltejs/kit/issues/10634). The issue explains why the reproduction exists.

## Run the Reproduction

The bugs that this reproduction shows off _do not_ happen on the development server. Instead, you need to build for production then preview the build. I believe this is because of the [bfcache](https://developer.mozilla.org/en-US/docs/Glossary/bfcache), which is disabled in development because hot module reloading on the dev server uses a web socket. This is mentioned in the GitHub issue.

```bash
npm run build
npm run preview
```