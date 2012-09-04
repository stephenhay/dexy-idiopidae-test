dexy-idiopidae-test
===================

Test for Ana Nelson's idiopidae-fork which should allow for multi-line comment syntax.

Idiopidae currently accepts things like:

    /// @export example

When using Dexy and exporting from CSS, this works fine. Except when using CSS preprocessors, which remove comments that use the single-line syntax when compiling.

If we want to export portions of the compiled CSS, I propose a syntax similar to:

    /*** @export example */

Ana's [idiopidae-fork](https://bitbucket.org/ananelson/idiopidae-fork/src) should allow for the following format:

    /*** @export "example" lang */

where `lang` is the language of the exported code (in our case CSS). The language attribute is required.

If this test is succesful, after running Dexy there will be an `index.html` file in Dexy's output folder which contains an example exported CSS snippet.

## Dependencies

- Dexy
- idiopidae-fork
- Pandoc

