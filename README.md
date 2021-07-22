# Programming Windows 5th edition source code

## Introduction

Source code contained in Charles Petzold's excellent [Programming Windows 5th edition](http://www.charlespetzold.com/pw5/). The source code is presented here for convenience (so you don't need to dig up the physical media of the book) and remains the copyright of the book authors. Consult `readme.txt` (the TXT that came with the book) for additional information.

## Changes

All samples have been updated to use Visual Studio 2019 and retargeted to use the latest Windows SDK. The old `*.dep`, `*.dsw`, and `*.dsp` files can be found in the earlier commits if you need them. That being said, the source code is two decades old and has been minimally retouched here. If you're after a more thorough overhaul of the codebase, [see here](https://github.com/recombinant/petzold-pw5e), or do a search on GitHub.

## Considerations

Most samples still function (credit to Microsoft and their emphasis on backwards compatibility), but some do not, particularly in Chapter 16 due to the requirement of hardware with 256-bit display pallete. Needless to say, decades after these samples were written, such hardware now exists mostly as a historical note of a bygone era in computing.

Some samples generate deprecation and security warnings upon compilation, and I recommend you heed those warnings if you intend to use any code in production. Remember that this is decades old Win32 code -- depending on what you're trying to do, more modern approaches such as [C++/WinRT](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/january/c-introducing-c-winrt), [wxWidgets](https://www.wxwidgets.org/), [Boost](https://www.boost.org/), [POCO C++](https://pocoproject.org/), or newer additions to the C++ standard library (C++11 onwards) may be more appropriate.

When using any Win32 code from this repo in production, always consult the [Windows API Index](https://docs.microsoft.com/en-us/windows/win32/apiindex/windows-api-list) for relevant and updated API usage notes, as some APIs may have since been deprecated or had their behaviour modified in newer versions of Windows.

## Additional resources

* [Build desktop Windows apps using the Win32 API](https://docs.microsoft.com/en-us/windows/win32/)
* [Get Started with Win32 and C++](https://docs.microsoft.com/en-us/windows/win32/learnwin32/learn-to-program-for-windows)
* [Windows API Index](https://docs.microsoft.com/en-us/windows/win32/apiindex/windows-api-list)
* [COM and ATL](https://docs.microsoft.com/en-us/cpp/atl/introduction-to-com-and-atl?view=msvc-160)
* [C++/WinRT](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/)
