**Visionary is a UI Framework to replace all existing UI Frameworks.**

* Visionary is Write Once Run Anywhere (WORA) in the sense that an abstract description of a UI written using the Visionary API will be sufficient to deploy to all widely-used forms of digital visualization. This includes, but is not limited to, web, desktop, mobile, virtual reality (VR), augmented reality (AR), and game engines. We also aim to support build targets that do not yet exist (ex. a GUI for neural lace wired to opitcal input nerve endings in the brain).

* Inspired by React and Elm, Visionary is component-based and uses an asynchronous message-passaging update system for uni-directional data flow and declarative rendering.

* Visionary will provide the ability to render native components and/or draw 2D and 3D graphics backed by the gfx project.

* A Virtual DOM inspired diffing system will be in charge of ensuring that as little Element/Widget destruction and initialization and as little graphics redrawing is done as possible.

* Inspired by Avalonia and React Primitives, Visionary's API will contain abstract control components which allow developers to express user interface layouts and controls from a high level that is platform agnostic.

* An `App` may contain `NativeComponent`s and `GraphicsComponent`s. `NativeComponent`s may contain `NativeComponent`s and `GraphicsComponent`s. `GraphicsComponent`s may only contain other `GraphicsComponent`s, of which there are `2DGraphicsComponent`s, and `3DGraphicsComponent`s.

* The abstracted control components are `NativeControlComponent`s which are a subtype of `NativeComponent`s and `GraphicsControlComponent`s which are a subtype of `GraphicsComponent`s; the first is natively rendered via the target platform's API, and the latter is drawn using the platform's native graphics library.

* All abstracted control components come with a default native theme, but any subtree of components may be assigned a different custom theme.

* Although the goal is to enable developers to write platform agnostic GUI, there is still first-class support for platform-specific logic and rendering. We attempt to ensure that such code stays as small and maintainable as possible.

 ### Why Rust?

* Rust is safer than other languages, both in terms of its static and strong type checking, and also because of its ability to prevent data races. These lead to the development of better-written software, which is what Visionary hopes for itself and its users to succeed in.

* Rust is not garbage collected (while also avoiding common C++ pitfalls). Rust has an efficiency advantage without compromising safety, and the resulting efficiency makes it an ideal candidate to run on all devices, some of which are more memory constrained than others.

* Rust has an advanced macro system which allows us to easily extend the Rust syntax to make expressing Visionary UI more intuitive and ergonomic.

* At the end of the day, we commit to the goal of a UI Framework which replaces all other UI Frameworks, and that commitment is larger than our commitment to the Rust language.

### Tooling TODOs:

* Modify Rust's VSCode extensions so all macros receive automatic syntax highlighting, auto-completion, error detection, reference-counting, refactoring, and breakpointing.

* Open-Source emulators for all target platforms with hot-reloading enabled for all.

* Extensive, pleasant-to-read documentation with code examples.
