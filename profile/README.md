## Macros and Metaprogramming

The ecosystem aiming to advance the typeclass-derivation and metaprogramming state of the art:

 * [**Hearth**](https://github.com/kubuszok/hearth) - the first standard library for macros: aims to make it easier to implement the most common
   macro-use cases, allow sharing the logic between 2.13 and 3.3+, establish good practices and patterns enabling better libraries UX
 * [**Kindlings**](https://github.com/kubuszok/kindlings) - the incubator for Hearth-based libraries. Let us test APIs in practice, let users
   test our solutions and give us feedback, shows how Hearth can be used in practice by both humans and LLMs

## Scala Game Engine (SGE)

The ecosystem aiming to port LibGDX and its extensions to Scala, to enable writing desktop/mobile/browser games in Scala,
with a native performance:

 * [**SGE**](https://github.com/kubuszok/sge) - Scala Game Engine and extensions - port of LibGDX and its extensions to Scala
 * [**SGE native providers**](https://github.com/kubuszok/sge-native-providers) - Rust ports of C++ libraries used by LibGDX and its extensions.
   Builds artifacts used by SGE via Panama on JVM and native binding on Scala Native
 * [**SGE ANGLE natives**](https://github.com/kubuszok/sge-angle-natives) - Builds ANGLE artifacts used by SGE via Panama on JVM and native binding on Scala Native

> [!note]
> SGE is a work in progress - it hasn't been released yet.

## Static Site Generator (SSG)

The ecosystem aiming to provide a static site generator for Scala, build on top of ports of established libraries to Scala
(allowing their usage with Scala/Scala Native/Scala.js):

 * [**SSG (Static Site Generator)**](https://github.com/kubuszok/ssg) - components porting established OSS libraries to Scala
   (flexmark-java, liqp, dart-sass, jekyll-minifier, ...)
 * [**SSE native providers**](https://github.com/kubuszok/sse-native-providers) - Bundled tree-sitter binaries and WASM
 * [**tree-sitter-natives**](https://github.com/kubuszok/tree-sitter-natives) - Builds trss-sitter artifacts used by SSE via Panama on JVM and native binding on Scala Native, and WASM on Scala.js

> [!note]
> SSG is a work in progress - it hasn't been released yet.

## Multiarch support enhancements

Utilities enabling: building Scala Native artifacts for multiple architectures on a single machine, packaging jlink for multiple operating systems,
shipping native components with your libraries to enable the above:

 * [**multiarch-scala**](https://github.com/kubuszok/multiarch-scala):
   - a sbt plugin for Scala Native that automatically extracts the libraries it links against and configures linker flags
   - a sbt plugin for Scala Native that uses Zig to build native artifacts for multiple architectures on the same machine
   - a sbt plugin for Scala JVM that packages jlink for multiple operating systems on the same machine
   - a CURL provider for Scala Native (so that your Scala Native libraries depending on libcurl without an additional installation)
 * [**curl-natives**](https://github.com/kubuszok/curl-natives) - Builds native curl bindings for Scala Native
 * [**scala-sax-parser**](https://github.com/kubuszok/scala-sax-parser) - cleanroom implementation of a SAX parser for Scala Native and Scala.js

> [!note]
> Multiarch-scala is a work in progress - it hasn't been released yet.

## Scala 2.13 <-> Scala 3 migration helpers

Libraries created to unblock cross-compilation of services writeen in Scala 2.13, which are relying on libraries missing
partial/full support on Scala 3.

Not aimed to use them as a permanent solution, but intended to be good enough to cross-compile existing 2.13 services with Scala 3,
migrate whole codebase gradually, cross-compiling 1 service at a time, and maintain dual release long enough to make dropping 2.13 safe.

 * [scala-newtype-compat](https://github.com/kubuszok/scala-newtype-compat) - compatibility layer which:
   - reimplements Scala 2 macro annotations as a compiler plugin
   - uses Scala 2.13 artifacts in Scala 3 via for3_use2.13 via our (empty) artifact
 * [refined-compat](https://github.com/kubuszok/refined-compat) - compatibility layer which:
   - reimplements `import eu.timepit.refined.auto._` using Hearth under `import hearth.refined.auto._` to allow 2.13/3 cross-compilation
   - reimplements `import eu.timepit.refined.refineMV` using Hearth under `import hearth.refined.refineMV` to allow 2.13/3 cross-compilation

> [!note]
> Migration helpers is a work in progress.
