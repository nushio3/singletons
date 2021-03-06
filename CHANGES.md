Changelog for singletons project
================================

0.9.3
-----

Fix export list of Data.Singletons.TH, again again.

Add `SEq` instances for `Nat` and `Symbol`.

0.9.2
-----

Fix export list of Data.Singletons.TH, again.

0.9.1
-----

Fix export list of Data.Singletons.TH.

0.9.0
-----

Make compatible with GHC HEAD, but HEAD reports core lint errors sometimes.

Change module structure significantly. If you want to derive your own
singletons, you should import `Data.Singletons.TH`. The module
`Data.Singletons` now exports functions only for the *use* of singletons.

New modules `Data.Singletons.Bool`, `...Maybe`, `...Either`, and `...List`
are just like their equivalents from `Data.`, except for `List`, which is
quite lacking in features.

For singleton equality, use `Data.Singletons.Eq`.

For propositional singleton equality, use `Data.Singletons.Decide`.

New module `Data.Singletons.Prelude` is meant to mirror the Haskell Prelude,
but with singleton definitions.

Streamline representation of singletons, resulting in *exponential* speedup
at execution. (This has not been rigorously measured, but the data structures
are now *exponentially* smaller.)

Add internal support for TypeLits, because the TypeLits module no longer
exports singleton definitions.

Add support for existential singletons, through the `toSing` method of
`SingKind`.

Remove the `SingE` class, bundling its functionality into `SingKind`.
Thus, the `SingRep` synonym has also been removed.

Name change: `KindIs` becomes `KProxy`.

Add support for singletonizing calls to `error`.

Add support for singletonizing empty data definitions.

0.8.6
-----

Make compatible with GHC HEAD, but HEAD reports core lint errors sometimes.

0.8.5
-----

Bug fix to make singletons compatible with GHC 7.6.1.

Added git info to cabal file.

0.8.4
-----

Update to work with latest version of GHC (7.7.20130114).

Now use branched type family instances to allow for promotion of functions
with overlapping patterns.

Permit promotion of functions with constraints by omitting constraints.

0.8.3
-----

Update to work with latest version of GHC (7.7.20121031).

Removed use of Any to simulate kind classes; now using KindOf and OfKind
from GHC.TypeLits.

Made compatible with GHC.TypeLits.

0.8.2
-----

Added this changelog

Update to work with latest version of GHC (7.6.1). (There was a change to
Template Haskell).

Moved library into Data.Singletons.

0.8.1
-----

Update to work with latest version of GHC. (There was a change to
Template Haskell).

Updated dependencies in cabal to include the newer version of TH.

0.8
---

Initial public release
