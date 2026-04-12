## Macros and Metaprogramming

The ecosystem aiming to advance the typeclass-derivation and metaprogramming state of the art:

 * [**Hearth**](https://github.com/kubuszok/hearth) - the first standard library for macros: aims to make it easier to implement the most common
   macro-use cases, allow sharing the logic between 2.13 and 3.3+, establish good practices and patterns enabling better libraries UX
 * [**Kindlings**](https://github.com/kubuszok/kindlings) - the incubator for Hearth-based libraries. Let us test APIs in practice, let users
   test our solutions and give us feedback, shows how Hearth can be used in practice by both humans and LLMs

## Scala Game Engine (SGE)

(Work in Progress)

The ecosystem aiming to port LibGDX and its extensions to Scala, to enable writing desktop/mobile/browser games in Scala,
with a native performance:

 * [**SGE**](https://github.com/kubuszok/sge) - Scala Game Engine and extensions - port of LibGDX and its extensions to Scala
 * [**SGE native components**](https://github.com/kubuszok/sge-native-components) - Rust ports of C++ libraries used by LibGDX and its extensions.
   Builds artifacts used by SGE via Panama on JVM and native binding on Scala Native

## Static Site Generator (SSG)

(Work in Progress)

The ecosystem aiming to provide a static site generator for Scala, build on top of ports of established libraries to Scala
(allowing their usage with Scala/Scala Native/Scala.js):

 * [**SSG (Static Site Generator)**](https://github.com/kubuszok/ssg) - components porting established OSS libraries to Scala
   (flexmark-java, liqp, dart-sass, jekyll-minifier, ...)

## Multiarch support enhancements

(Work in Progress)

Utilities enabling: building Scala Native artifacts for multiple architectures on a single machine, packaging jlink for multiple operating systems,
shipping native components with your libraries to enable the above:

 * [**sbt-multi-arch-release**](https://github.com/kubuszok/sbt-multi-arch-release):
   - a sbt plugin that automaticallyextracts for Scala Native the libraries it links against and configures linker flags
   - a sbt plugin that uses Zig to build native artifacts for multiple architectures
   - a sbt plugin that packages jlink for multiple operating systems
   - a CURL provider for Scala Native (so that your Scala Native libraries depending on libcurl without an additional installation)
 * [**curl-natives**](https://github.com/kubuszok/curl-natives) - Builds native curl bindings for Scala Native
