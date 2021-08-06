# SASS @extend bug

This repo gives a simple demonstration of an apparenty bug in the dart implementation of sass (the `sass` npm package).
Addtionally it demonstrates that the bug did not exist within the libsass-based implementation (the `node-sass` npm
package).

# Setup
Run `yarn install` to install dependencies (`sass` and `node-sass`).

# Demonstration
The problematic scss input is present in the `index.scss` file. Run `yarn build` to
see the output when this file is processed with the `sass` compiler (dart-sass). Run `yarn node-sass-build` to see
the output when the file is process with the `node-sass` compiler. The `node-sass` compiler gives the output that I
would expect - it includes the disabled hover styles. The `sass` output does not include the disabled hover styles.
