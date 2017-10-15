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
* JIT compilation upon code edit, or just projectional view/edit? (is this the same thing?)
* Edit code without breaking closures (like JavaScript fails to do)
* Instead of hiding things (like closures) or enforcing restrictions (types, access-levels), expose ALL things for maximum potential, and rely on good structure & practice to make things clear
  * Related: Linda Rising's article; Jane Jacobs (read about apartments on the wiki page)
* Still generate compiled programs, but a bootstrapped self-contained tool as a better alternative to "source code"
* No external references in objects (or just in "code"), for better serialization. ("message passing")
* Runtime execution somehow exists in some inspectable form, so it could be "paused", modifed, serialized, and resumed
  * Actors that can be sent (or send themselves) across systems, and keep running afterward
* Distinction between objects and networked computers is diminished
* Do not get stuck on specific implementation choices if it can be changed later ("worse is better")
* Code consists of imperative commands rather than declarative statements that must be compiled & analyzed. Declarative entites just "exist" inline.
* Loosely coupled code -> named references into a "context" object
* All objects are part of some tree, and the whole system is one tree
* Separate storage of execution state ("context") from code
  * Any runtinme operation can derive from just modeling the execution state directly
  * Continuation Passing Style?
* Potential of LISP is generally overlooked, and it is used as JUST a programming language
* Macro-expansion assumes a compilation phase
* Not a MetaObject Protocol, but a MMOP that is its own MMMOP
  * Lisp Macro expansion does this because the macro language is the same as the target-languages; and thus you can have macro-macros, etc. Apply this idea to UI & code: if they are "the same thing", then ... voila!
* No need for an OS
* Software Archeology: self-contained system that makes its own bootstrapping & running self-evident: http://www.vpri.org/pdf/tr2015004_cuneiform.pdf
* Software is already its own tool (software makes, edits, and runs software)
* Stop making programming better for programmers, and make computering better for users (note: have we even discovered what "computer" can mean? Can we open the door to let users do that discovering?)
* Replace concept of "compile time" with JIT compilation (i.e. compilation on demand at runtime). How is this any different than any other normal code transforming data (especially if code and data are the same)?
* Editing a feature in a software tool makes that feature *immediately* available (take affect) within the tool, rather than rebuilding a new artifact from edited code.
* "Restricted OO" (see http://fulloo.info)
* Making software componentized/modular is only meaningful if the abstractions are whole and proper. And if they are, then the composability becomes more than just a nice property of source code, but something that can be exposed to the end-user through a UI at runtime (drag-and-drop software composition through a UI)
* If all objects have a UI metaphor, then maybe you don't need a UI for everything? It's like a UI equivalent of a command-prompt? (API x UI = AUI?)
* A "Grammar" of visual (and behavioral) pieces, and not just textual "language". (Expand this idea to "macros"?)
* Embedded DSLs and interpreters within existing ones, but all running at the "root" level

