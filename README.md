# Programming Windows 5th edition source code

Source code contained in Charles Petzold's excellent [Programming Windows 5th edition](http://www.charlespetzold.com/pw5/). The source code is presented here for convenience (so you don't need to dig up the physical media of the book) and remains the copyright of the book authors. Consult `readme.txt` (the TXT that came with the book) for additional information.

All samples have been updated to use Visual Studio 2019 and retargeted to use the latest Windows SDK. The old `*.dep`, `*.dsw`, and `*.dsp` files can be found in the earlier commits if you need them. That being said, the source code is two decades old and has been minimally retouched here. Most samples still function (credit to Microsoft and their emphasis on backwards compatibility), but some do not, particularly in Chapter 16 due to the requirement of a 256-bit display pallete (hardware that has long since faded away). Some samples may generate deprecation and security warnings upon compilation, and I recommend you heed those warnings if you intend to use any code in production.

If you're after a more thorough overhaul of the codebase, [see here](https://github.com/recombinant/petzold-pw5e), or do a search on GitHub.

__________________________________________________________________

                Programming Windows, Fifth Edition

                        by Charles Petzold

            Copyright (c) 1999 by Microsoft Corporation
          Portions copyright (c) 1999 by Charles Petzold
                        All Rights Reserved
___________________________________________________________________
