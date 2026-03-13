This PR adds types for [Glide](https://glide-browser.app), a Firefox fork that supports a TypeScript config.

Users currently get the types through the browser automatically writing `glide.d.ts` files as a sibling to their config file. This works great for users directly interfacing with the browser but doesn't work as well for anyone that wants to package a config file separately (e.g. a plugin).

The types in this PR come from two main places:
- https://github.com/glide-browser/glide/blob/da17cf9134ab8e56d0362d9284bc3211d7632858/src/glide/browser/base/content/glide.d.ts
- https://github.com/glide-browser/webextension-types

Which are then bundled into a single file for easier distribution. The `index.d.ts` file included here is the exact same one packaged directly with the browser.

I didn't include tests here because I already have my own type tests https://github.com/glide-browser/glide/blob/main/src/glide/browser/base/content/test/config/types/config.ts

Please fill in this template.

- [ ] Use a meaningful title for the pull request. Include the name of the package modified.
- [ ] Test the change in your own code. (Compile and run.)
- [ ] [Add or edit tests](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#my-package-teststs) to reflect the change.
- [ ] Follow the advice from the [readme](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#make-a-pull-request).
- [ ] Avoid [common mistakes](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#common-mistakes).
- [ ] [Run `pnpm test <package to test>`](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#running-tests).

If adding a new definition:

- [ ] The package does not already provide its own types, or cannot have its `.d.ts` files generated via `--declaration`
- [ ] If this is for an npm package, match the name. If not, do not conflict with the name of an npm package.
- [ ] Create it with `dts-gen --dt`, not by basing it on an existing project.
- [ ] Represents shape of module/library [correctly](https://www.typescriptlang.org/docs/handbook/declaration-files/library-structures.html)
- [x] `tsconfig.json` [should have](https://github.com/DefinitelyTyped/DefinitelyTyped/blob/master/README.md#tsconfigjson) `noImplicitAny`, `noImplicitThis`, `strictNullChecks`, and `strictFunctionTypes` set to `true`.
