# Keywords

Rust divides keywords into three categories:

* [strict](#strict-keywords)
* [reserved](#reserved-keywords)
* [weak](#weak-keywords)

## Strict keywords

These keywords can only be used in their correct contexts. They cannot
be used as the names of:

* [Items]
* [Variables] and function parameters
* Fields and [variants]
* [Type parameters]
* Lifetime parameters or [loop labels]
* [Macros] or [attributes]
* [Macro placeholders]
* [Crates]

> **<sup>Lexer:<sup>**\
> KW_AS             : `as`\
> KW_BREAK          : `break`\
> KW_CONST          : `const`\
> KW_CONTINUE       : `continue`\
> KW_CRATE          : `crate`\
> KW_ELSE           : `else`\
> KW_ENUM           : `enum`\
> KW_EXTERN         : `extern`\
> KW_FALSE          : `false`\
> KW_FN             : `fn`\
> KW_FOR            : `for`\
> KW_IF             : `if`\
> KW_IMPL           : `impl`\
> KW_IN             : `in`\
> KW_LET            : `let`\
> KW_LOOP           : `loop`\
> KW_MATCH          : `match`\
> KW_MOD            : `mod`\
> KW_MOVE           : `move`\
> KW_MUT            : `mut`\
> KW_PUB            : `pub`\
> KW_REF            : `ref`\
> KW_RETURN         : `return`\
> KW_SELFVALUE      : `self`\
> KW_SELFTYPE       : `Self`\
> KW_STATIC         : `static`\
> KW_STRUCT         : `struct`\
> KW_SUPER          : `super`\
> KW_TRAIT          : `trait`\
> KW_TRUE           : `true`\
> KW_TYPE           : `type`\
> KW_UNSAFE         : `unsafe`\
> KW_USE            : `use`\
> KW_WHERE          : `where`\
> KW_WHILE          : `while`

|Keyword|Tested|Source|
|---|---|---|
|as|✔️|.\tests\ui\parser\keyword-as-as-identifier.rs|
|break|✔️|.\tests\ui\parser\keyword-break-as-identifier.rs|
|const|✔️|.\tests\ui\parser\keyword-const-as-identifier.rs|
|continue|✔️|.\tests\ui\parser\keyword-continue-as-identifier.rs|
|crate|✔️|.\tests\ui\rfcs\rfc-2126-crate-paths\keyword-crate-as-identifier.rs|
|else|✔️|.\tests\ui\parser\keyword-else-as-identifier.rs|
|enum|✔️|.\tests\ui\parser\keyword-enum-as-identifier.rs|
|extern|✔️|.\tests\ui\keyword\extern\keyword-extern-as-identifier-expr.rs <br> .\tests\ui\keyword\extern\keyword-extern-as-identifier-pat.rs <br> .\tests\ui\keyword\extern\keyword-extern-as-identifier-type.rs <br> .\tests\ui\keyword\extern\keyword-extern-as-identifier-use.rs|
|false|✔️|.\tests\ui\keyword\keyword-false-as-identifier.rs|
|fn|✔️|.\tests\ui\parser\keyword-fn-as-identifier.rs|
|for|✔️|.\tests\ui\parser\keyword-for-as-identifier.rs|
|if|✔️|.\tests\ui\parser\keyword-if-as-identifier.rs|
|impl|✔️|.\tests\ui\parser\keyword-impl-as-identifier.rs|
|in|✔️|.\tests\ui\parser\keyword-in-as-identifier.rs|
|let|✔️|.\tests\ui\parser\keyword-let-as-identifier.rs|
|loop|✔️|.\tests\ui\parser\keyword-loop-as-identifier.rs|
|match|✔️|.\tests\ui\parser\keyword-match-as-identifier.rs|
|mod|✔️|.\tests\ui\parser\keyword-mod-as-identifier.rs|
|move|✔️|.\tests\ui\parser\keyword-move-as-identifier.rs|
|mut|✔️|.\tests\ui\parser\keyword-mut-as-identifier.rs|
|pub|✔️|.\tests\ui\parser\keyword-pub-as-identifier.rs|
|ref|✔️|.\tests\ui\parser\keyword-ref-as-identifier.rs|
|return|✔️|.\tests\ui\parser\keyword-return-as-identifier.rs|
|self|||
|Self|✔️|.\tests\ui\keyword\keyword-self-as-identifier.rs|
|static|✔️|.\tests\ui\parser\keyword-static-as-identifier.rs|
|struct|✔️|.\tests\ui\parser\keyword-struct-as-identifier.rs|
|super|✔️|.\tests\ui\keyword\keyword-super-as-identifier.rs|
|trait|✔️|.\tests\ui\parser\keyword-trait-as-identifier.rs|
|true|✔️|.\tests\ui\keyword\keyword-true-as-identifier.rs|
|type|✔️|.\tests\ui\parser\keyword-type-as-identifier.rs|
|unsafe|✔️|.\tests\ui\parser\keyword-unsafe-as-identifier.rs|
|use|✔️|.\tests\ui\parser\keyword-use-as-identifier.rs|
|where|✔️|.\tests\ui\parser\keyword-where-as-identifier.rs|
|while|✔️|.\tests\ui\parser\keyword-while-as-identifier.rs|

The following keywords were added beginning in the 2018 edition.

> **<sup>Lexer 2018+</sup>**\
> KW_ASYNC          : `async`\
> KW_AWAIT          : `await`\
> KW_DYN            : `dyn`

|Keyword|Tested|Source|
|---|---|---|
|async|||
|await|||
|dyn|||

## Reserved keywords

These keywords aren't used yet, but they are reserved for future use. They have
the same restrictions as strict keywords. The reasoning behind this is to make
current programs forward compatible with future versions of Rust by forbidding
them to use these keywords.

> **<sup>Lexer</sup>**\
> KW_ABSTRACT       : `abstract`\
> KW_BECOME         : `become`\
> KW_BOX            : `box`\
> KW_DO             : `do`\
> KW_FINAL          : `final`\
> KW_MACRO          : `macro`\
> KW_OVERRIDE       : `override`\
> KW_PRIV           : `priv`\
> KW_TYPEOF         : `typeof`\
> KW_UNSIZED        : `unsized`\
> KW_VIRTUAL        : `virtual`\
> KW_YIELD          : `yield`

|Keyword|Tested|Source|
|---|---|---|
|abstract|✔️|.\tests\ui\parser\keyword-abstract.rs|
|become|||
|box|✔️|.\tests\ui\parser\keyword-box-as-identifier.rs|
|do|||
|final|✔️|.\tests\ui\parser\keyword-final.rs|
|macro|||
|override|✔️|.\tests\ui\parser\keyword-override.rs|
|priv|||
|typeof|✔️|.\tests\ui\parser\keyword-typeof.rs|
|unsized|||
|virtual|||
|yield|||

The following keywords are reserved beginning in the 2018 edition.

> **<sup>Lexer 2018+</sup>**\
> KW_TRY   : `try`

|Keyword|Tested|Source|
|---|---|---|
|try|✔️|.\tests\ui\parser\keyword-try-as-identifier-edition2018.rs|

## Weak keywords

These keywords have special meaning only in certain contexts. For example, it
is possible to declare a variable or method with the name `union`.

* `macro_rules` is used to create custom [macros].
* `union` is used to declare a [union] and is only a keyword when used in a
  union declaration.
* `'static` is used for the static lifetime and cannot be used as a [generic
  lifetime parameter] or [loop label]

  ```compile_fail
  // error[E0262]: invalid lifetime parameter name: `'static`
  fn invalid_lifetime_parameter<'static>(s: &'static str) -> &'static str { s }
  ```
* In the 2015 edition, [`dyn`] is a keyword when used in a type position
  followed by a path that does not start with `::`.

  Beginning in the 2018 edition, `dyn` has been promoted to a strict keyword.

> **<sup>Lexer</sup>**\
> KW_MACRO_RULES    : `macro_rules`\
> KW_UNION          : `union`\
> KW_STATICLIFETIME : `'static`
>
> **<sup>Lexer 2015</sup>**\
> KW_DYN            : `dyn`

[items]: items.md
[Variables]: variables.md
[Type parameters]: types/parameters.md
[loop labels]: expressions/loop-expr.md#loop-labels
[Macros]: macros.md
[attributes]: attributes.md
[Macro placeholders]: macros-by-example.md
[Crates]: crates-and-source-files.md
[union]: items/unions.md
[variants]: items/enumerations.md
[`dyn`]: types/trait-object.md
[loop label]: expressions/loop-expr.md#loop-labels
[generic lifetime parameter]: items/generics.md
