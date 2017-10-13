**List of relevent concepts for designing relevant solutions**

* A tool that is its own live-editor
* Bootstrap a minimum implementation from which something better can be made (e.g. some initial design decisions dont matter if they can be made fluid)
* Software that can evolve or be reshaped into something new or different as needed
* Blurring the line between compile-time and runtime execution, script and executable, meta and non-meta.
* Blurring the line between programming (code) and user interaction (UI)
* Working directly with the intended model (e.g. AST or nodes of entities), rather than a *representation* of it (e.g. textual code)
  * No need for parsing
* Not imposing a prescriptive way of doing things (e.g. programming language, code frameworks, set-in-stone UI, etc.)
* Instead of many different things with different interfaces and specifications, have fewer general things.
  * An AST structure can model both code & data, but also (for example) files & folders, or settings.
* Projectional editing
* Simplicity over complexity
* Simplicity of underlying structure, or of mechanism for creating it? Maybe there should be no (or little) distinction between the two
  * Compare JavaScript to other languages: Most declarations are not fundamentally different than any other imperative code.
* Think of programming language as a way to specify a program using a grammar. What if instead of a grammar, you used an API to create program constructs and make API calls to manipulate, validate, and build it? It would be very easy to extend however you like. Also, extend this idea to UI
* Specify structure, or specify process that generates structure?
* Universal support for viewing, editing, and serializing a common object model (AST)
* Rather than depending on separate things (programming language, IDE, editor, etc.), each piece of software should be its own self-contained tool for doing all this, capable of editing its own "language"/compiler (if relevent), UI, etc.
* Strong sense of identity (e.g. references instead of names)
* Dynamic structure/language versus static (that is, making structure implicit in itself rather than "stripped away" or held to a rigid calculus)
  * Related to software having its own self-contained editor, language, compiler, and UI
  * Be aware of pre-mature optimization that makes decisions (or sets things in stone) too early
    * There are always techniques to overcome inefficiencies, such as caching of lookups.
* Making decisions (or allowing them to be made) based on context. (Context-dependent language, UI, etc; software that works a certain way that's best for itself, rather than trying to choose a prescriptive way to "do everything")
* Modeling & editing structure as-is, or modeling and editing a generative process and replacing the old thing by regenerating it.
* Programming via interaction (e.g. capturing operations as steps of UI operations, rather than trying to visualize a "flow" of operations). Idea taken from Bret Victor's "Drawing Dynamic Visualizations".
  * That is, not a flat look-at-it-all-at-once model of exeuction, but a dynamic interactive model for exploring it. Also see Bret Victor's "Media for Thinking the Unthinkable"
* An entire system composed of objects that can be inspected and manipulated by the user at runtime
* Alan Kay's concept of objects being a recursion of the notion of "computer"
  * Object (interface), UI, API ... These are all really the same thing
* OO is about objects, not about classes (Jim Coplien & DCI)
* Bootstrapping: compiler/system written in "itself", and can self re-define
  * Built-in compilers/translators/serializers that can re-compile the system/runtime to another platform, and each compiler "comes with" because it is written in the language of the system. ("Ultron")
* Automatic JIT compilation, or compiling only key components (which?)?
* A basic UI substrate from which anything can be put together (like how any structure can be built from the same object-model)
  * Concept of graphics primitives, or of UI primitives (e.g. boxes), each with their own relative transformations
* A way to map code (and other things) to custom UIs/views
* To prototype (or class) objects, or not to?
* Developing more of a runtime model (e.g. a whole system) rather than just a language (e.g. dependency on compiler)
* AST means nothing is every "compiled" down to machine level, but instead there is a kernel (written or mirrored in itself)
