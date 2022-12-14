# π¦πΈοΈ `wasm-pack-template`

A template for kick starting a Rust and WebAssembly project using
[`wasm-pack`](https://github.com/rustwasm/wasm-pack).

This template is designed for compiling Rust libraries into WebAssembly and
publishing the resulting package to NPM.

* Want to use the published NPM package in a Website? [Check out
  `create-wasm-app`.](https://github.com/rustwasm/create-wasm-app)
* Want to make a monorepo-style Website without publishing to NPM? Check out
  [`rust-webpack-template`](https://github.com/rustwasm/rust-webpack-template)
  and/or
  [`rust-parcel-template`](https://github.com/rustwasm/rust-parcel-template).

## π Batteries Included

* [`wasm-bindgen`](https://github.com/rustwasm/wasm-bindgen) for communicating
  between WebAssembly and JavaScript.
* [`console_error_panic_hook`](https://github.com/rustwasm/console_error_panic_hook)
  for logging panic messages to the developer console.
* [`wee_alloc`](https://github.com/rustwasm/wee_alloc), an allocator optimized
  for small code size.

## π΄ Usage

### π Use `cargo generate` to Clone this Template

[Learn more about `cargo generate` here.](https://github.com/ashleygwilliams/cargo-generate)

```
cargo generate --git https://github.com/rustwasm/wasm-pack-template.git --name my-project
cd my-project
```

### π οΈ Build with `wasm-pack build`

```
wasm-pack build
```

### π¬ Test in Headless Browsers with `wasm-pack test`

```
wasm-pack test --headless --firefox
```

### π Publish to NPM with `wasm-pack publish`

```
wasm-pack publish
```

## Notes

### Creating

```sh
cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

### Building

```sh
wasm-pack build
```

### Web Page

```sh
npm init wasm-app www

cd www/
npm install

cd ../pkg/
npm link

cd ../www/
npm link wasm-game-of-life
```

Update `index.js` with filename changes.

### Serve Locally

```sh
cd www/
npm run start
```

### Test

```sh
wasm-pack test --chrome --headless
wasm-pack test --firefox --headless
```
