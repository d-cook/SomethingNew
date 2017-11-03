**List of relevent concepts for designing relevant solutions**

*(TODO: Add concepts gathered from materials listed in Resources.md)*

#### Moldable software
* Software (tools) that can evolve or be reshaped into something new or different at will (by the end-user)
* The software tool is its own live-editor, and can be insected and modified in place (without "rebuilding")
* "Strong References": Entities (in code) are referenced directly rather than by name. Changes to the entity (e.g. rename) are immediately reflected (transparaent) everywhere that the entity is used.
* Ability to edit code (at runtime) without breaking context (e.g. JavaScript closures are broken when functions are edited)

#### Self-Ownership
* Abstract: Software entities define their own creation, language, UI, editor, etc. in a self-evident way
* The software tool is its own live-editor, and can be insected and modified in place (without "rebuilding")
* Surprising that this is not already common, since the tool for making & editing software is ... ***software***
* Bootstrapping: compiler/system that is written in "itself", and can self re-define
* System with built-in compiler / translator / serializer that can re-compile the system/runtime to another platform, and each compiler "comes with" because it is written in the language of the system. ("Ultron")

#### Everything as Objects
* Alan Kay: objects as a recursion of the notion of "computer"
* Everything (code, data, UI, runtime) is made of nestable "objects" that can be inspected and modified in place
* All objects are part of the same "object-tree", with the "root node" being the entire system
* Work directly with intented model (structure) of things, rather than a *representation* of that structure
  * Code is manipulated directly in [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree) form, rather than [Parsed](https://en.wikipedia.org/wiki/Parsing#Computer_languages) from text.
  * Code can be generated & manipulated directly at runtime (by the user, or programmatically)
* A universal tool can be used to view and edit everything, since it all shares a common representation
* An AST structure can model both code & data, but also (for example) files & folders, or settings.

#### Message Passing
* Operations between objects (code) are all "messages"
* Alan Kay: objects as a recursion of the notion of "computer"
* Blurred distinction between objects and networked computers (Alan Kay's notion of objects)
* "Strong References" are avoided, so that objects are decoupled (better for composition & serialization)

#### Stepping Stones ("Worse is Better")
* "Everything as Objects": Bootstrap a minimal implementation from which something better can be made
  * Initial decision decisions don't matter much if they can be made easily (fluidly) changeable

#### Trade Restrictions for Open-ness
* Respect for the human element, and not restricted mechanisms, does the most to encourage good design. Related [Resources](https://github.com/d-cook/SomethingNew/blob/master/Resources.md): Linda Rising; Jane Jacobs
* Not imposing a prescriptive way of doing things (e.g. programming language, code frameworks, set-in-stone UI, etc.)
* Instead of hiding things (like closure contexts) or enforcing restrictions (static types, access-level modifiers), expose ALL things for maximum potential, and rely on good structure & practice to make things clear
* Late bound & Dynamic- instead of static-typing (i.e. structure is implicit rather than "stripped away" or held to a rigid calculus)
* Avoid pre-mature optimizations that make decisions / set things in stone too early
* Fewer "different kinds" of things, and more general (and simpler) common things / representations / tools.
* Simple underlying structure for representing many things ("Everything as Objects")
* Context-based decisions, behaviors, language, UI, etc. rather than prescribing "one for all" ("Self-Ownership")

----

*Everything above has been refined & organized. Everything below has yet to be.*

----

#### Blurring the line between compile-time and runtime execution, script and executable, meta and non-meta.
#### Blurring the line between programming (code) and user interaction (UI)
#### Projectional editing
#### Simplicity over complexity
#### Simplicity of underlying structure, or of mechanism for creating it? Maybe there should be no (or little) distinction between the two
  * Compare JavaScript to other languages: Most declarations are not fundamentally different than any other imperative code.
#### Think of programming language as a way to specify a program using a grammar. What if instead of a grammar, you used an API to create program constructs and make API calls to manipulate, validate, and build it? It would be very easy to extend however you like. Also, extend this idea to UI
#### Specify structure, or specify process that generates structure?
#### Rather than depending on separate things (programming language, IDE, editor, etc.), each piece of software should be its own self-contained tool for doing all this, capable of editing its own "language"/compiler (if relevent), UI, etc.
#### Modeling & editing structure as-is, or modeling and editing a generative process and replacing the old thing by regenerating it.
#### Programming via interaction (e.g. capturing operations as steps of UI operations, rather than trying to visualize a "flow" of operations). Idea taken from Bret Victor's "Drawing Dynamic Visualizations".
  * That is, not a flat look-at-it-all-at-once model of exeuction, but a dynamic interactive model for exploring it. Also see Bret Victor's "Media for Thinking the Unthinkable"
#### Object (interface), UI, API ... These are all really the same thing
#### OO is about objects, not about classes (Jim Coplien & DCI)
#### Automatic JIT compilation, or compiling only key components (which?)?
#### A basic UI substrate from which anything can be put together (like how any structure can be built from the same object-model)
  * Concept of graphics primitives, or of UI primitives (e.g. boxes), each with their own relative transformations
#### A way to map code (and other things) to custom UIs/views
#### To prototype (or class) objects, or not to?
#### Developing more of a runtime model (e.g. a whole system) rather than just a language (e.g. dependency on compiler)
#### AST means nothing is every "compiled" down to machine level, but instead there is a kernel (written or mirrored in itself)
#### JIT compilation upon code edit, or just projectional view/edit? (is this the same thing?)
#### Still generate compiled programs, but a bootstrapped self-contained tool as a better alternative to "source code"
#### Runtime execution somehow exists in some inspectable form, so it could be "paused", modifed, serialized, and resumed
  * Actors that can be sent (or send themselves) across systems, and keep running afterward
#### Do not get stuck on specific implementation choices if it can be changed later ("worse is better")
#### Code consists of imperative commands rather than declarative statements that must be compiled & analyzed. Declarative entites just "exist" inline.
#### Loosely coupled code -> named references into a "context" object
#### Separate storage of execution state ("context") from code
  * Any runtinme operation can derive from just modeling the execution state directly
  * Continuation Passing Style?
#### Potential of LISP is generally overlooked, and it is used as JUST a programming language
#### Macro-expansion assumes a compilation phase
#### Not a MetaObject Protocol, but a MMOP that is its own MMMOP
  * Lisp Macro expansion does this because the macro language is the same as the target-languages; and thus you can have macro-macros, etc. Apply this idea to UI & code: if they are "the same thing", then ... voila!
#### No need for an OS
#### Software Archeology: self-contained system that makes its own bootstrapping & running self-evident: http://www.vpri.org/pdf/tr2015004_cuneiform.pdf
#### Stop making programming better for programmers, and make computering better for users (note: have we even discovered what "computer" can mean? Can we open the door to let users do that discovering?)
#### Replace concept of "compile time" with JIT compilation (i.e. compilation on demand at runtime). How is this any different than any other normal code transforming data (especially if code and data are the same)?
#### "Restricted OO" (see http://fulloo.info)
#### Making software componentized/modular is only meaningful if the abstractions are whole and proper. And if they are, then the composability becomes more than just a nice property of source code, but something that can be exposed to the end-user through a UI at runtime (drag-and-drop software composition through a UI)
#### If all objects have a UI metaphor, then maybe you don't need a UI for everything? It's like a UI equivalent of a command-prompt? (API x UI = AUI?)
#### A "Grammar" of visual (and behavioral) pieces, and not just textual "language". (Expand this idea to "macros"?)
#### Embedded DSLs and interpreters within existing ones, but all running at the "root" level
#### Instead of using macros to convert from a good representative to an obscure one, choose a good underlying representation to begin with, and a good UI tool for showing & editing it (see "Magic Ink"). The underlying representation can be flexible by allowing context-specific evaluators.
#### There is a way to do this "stuff" and / or create other powerful software tools and engines, WITHOUT a huge pile of frameworks and lots of very specific complicated parts. Once we make such a system, we may be able to find a minimal set of patterns and process that would allow anyone to" bootsrap" almost anything on almost any system, from almost nothing.
#### Object-Oriented CPU. Fundamental object-operations (get, set, delete, etc) are supported by hardware. Imagine something like JavaScript running on bare metal, and all the layers of software that would cut out. This could potentially be much more efficient than traditional statically-typed compiled languages.
#### Tool support for a recorder view of the program which supports programming and debugging by demonstration: record, unplay, play, step, unstep, undo and cut (forward) of actions.  Be able to program with the previous operations.  Store a log or trace of operations in the live-editor for use with the PbD system.  Support research into sequence clustering of code, imitation learning and one-shot imitation learning, to model the programmers mind.
