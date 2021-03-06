CHANGELOG

---

1.1

- @each support #36

---

1.0.1

- Update to Esprima 1.2.2 #28
- Traverser's skip array causing 6% slowdown #29
- Add ability for typealias / typedef #30
- Classes can be superclasses of each other #23
- Dynamic property prevents synthesis of following properties #35
- @synthesize should always make a backing ivar #34
- Add documentation for $oj_oj #33
- Add 'temp' dependency #32
- Support protocols and typed arrays #31

---

1.0.0 (Released 2014-11-04)

1.x is a backwards incompatible release, with a focus on enhancing runtime performance.

Removed:

  - Removed separate `ojsqueeze` command-line tool.  The squeezer is now integrated directly into `ojc` (#8)
  - Removed `+initialize` and `+load`.  This allows faster message dispatch.  (#12)
  - Removed `--use-const` and `--use-enum` compiler flags.  Use the new `@const` and `@enum` instead (#11) 
  - Removed `--use-prefix` compiler flag.  Prefixes are always used.  (#6)
  - Removed `--always-message` compiler flag.  Replaced with `--debug-message-send`.

Enhancements:

  - Faster message dispatch:  Direct calls are used more often than `oj.msgSend` (#10)
  - Inline `+[Foo alloc]` calls as `new Foo()`
  - Updated parser to Esprima 1.1 (#9)
  - Unique JavaScript symbol names for methods (#20)
  - Warn about unused ivars (#22)

Additions:

  - New `@const` and `@enum`
  - Integration of squeezer directly into ojc.  This allows more squeeze-time optimizations.
  - Documentation for runtime (#7)
  - Documentation for compiler API
  - Source map support (#13)
  - Support for jshint (#14)

Bug Fixes:

  - Duplicate @implementation of same class should throw error (#15)
  - (3.14 * [[self foo] bar]) results in NaN (#16)
  - Automatic synthesis of properties produces too many ivars (#19)
  - ivars that are @enum types should be initialized to 0. (#21)

---
