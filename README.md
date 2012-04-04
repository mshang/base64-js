See the [demo](http://mshang.ca/base64-js/).

This script encodes to and decodes from base64. It allows you to specify a few parameters:

* The non-alphanumeric characters.
* The padding character, or lack thereof.
* 8-bit or 16-bit string input.

Your standard base64 uses `+` and `/` as the non-alphanumeric characters, and `=` as the padding character. Now say you want base64url. No problem. Just use the following settings:

    base64.settings.char62 = "-";
	base64.settings.char63 = "_";
	base64.settings.pad = null;

In terms of input, 8 bits is the standard. However, with only 8 bits, you can't encode Chinese characters, for example. 16 bits gives lengthier output, but allows you to preserve full Unicode fidelity as Javascript strings themselves are just arrays of 16-bit values.

test.html contains a few tests.