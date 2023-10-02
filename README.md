# Programming Windows 5th edition source code

## Introduction

Source code contained in [Charles Petzold's](https://www.charlespetzold.com/) excellent [Programming Windows 5th edition](http://www.charlespetzold.com/pw5/). No representation is made that the source code belongs to me, it's simply reproduced here for convenience (so you don't need to dig up the physical media of the book) and remains the copyright of Charles Petzold. Consult `readme.txt` (the TXT that came with the book) for additional information.

## Building

You'll need Visual Studio 2022 with the _Desktop development with C++_ workload installed. Some samples use MFC, so you'll need to install the _C++ MFC for latest v143 build tools (x86 & x64)_ Visual Studio component to build them (MFC is not installed by default in newer versions of Visual Studio). You should then be able to open any of the VS solution files and immediately build them. It may be possible to open the VS solution files using older (but still modern) versions of Visual Studio, but I've not tested this.

## Changes

All samples have been updated to use Visual Studio 2022 and retargeted to use the latest Windows SDK. An invalid free that was causing crashes in Chapter 9's Environ sample has been fixed, and a separate crash in Chapter 10's PoePoem sample has also been fixed. The old `*.dep`, `*.dsw`, and `*.dsp` files can be found in the earlier commits if you need them. That being said, the source code is two decades old and has been minimally retouched here. If you're after a more thorough overhaul of the codebase, [see here](https://github.com/recombinant/petzold-pw5e), or do a search on GitHub.

## Considerations

Most samples still function (credit to Microsoft and their emphasis on backwards compatibility), but some do not, particularly in Chapter 16 due to the requirement of hardware with 256-bit display pallete. Needless to say, decades after these samples were written, such hardware now exists mostly as a historical note of a bygone era in computing.

Some samples generate deprecation and security warnings upon compilation, and I recommend you heed those warnings if you intend to use any code in production. Remember that this is decades old Win32 code -- depending on what you're trying to do, more modern approaches such as [C++/WinRT](https://learn.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/), [WinUI 3](https://docs.microsoft.com/en-us/windows/apps/winui/winui3/), [wxWidgets](https://www.wxwidgets.org/), [Qt](https://www.qt.io/), [Ultimate++](https://www.ultimatepp.org/), [Boost](https://www.boost.org/), [POCO C++](https://pocoproject.org/), or newer additions to the C++ standard library (C++11 onwards) may be more appropriate.

When using any Win32 code from this repo in production, always consult the [Windows API Index](https://docs.microsoft.com/en-us/windows/win32/apiindex/windows-api-list) for relevant and updated API usage notes, as some APIs may have since been deprecated or had their behaviour modified in newer versions of Windows.

## Additional resources

### General

* [The Windows API Index](https://docs.microsoft.com/en-us/windows/win32/apiindex/windows-api-list)
* [Jeffrey Richter and Christophe Nasarre's Windows via C/C++ 5th edition](https://www.microsoftpressstore.com/store/windows-via-c-c-plus-plus-9780735639218). An excellent book on Windows system programming. [Source code repo here](https://github.com/yottaawesome/windows-via-c-cpp).

### Samples

* [Microsoft's Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples)
* [Microsoft's C++ samples](https://docs.microsoft.com/en-us/samples/browse/?languages=cpp)

### Related technologies

* [Microsoft's COM and ATL](https://docs.microsoft.com/en-us/cpp/atl/introduction-to-com-and-atl)
* [Microsoft's Universal Windows Platform](https://learn.microsoft.com/en-us/windows/uwp/get-started/)
* [Microsoft's C++/WinRT](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/). A modern C++17 projection over the Windows Runtime APIs.
* [Microsoft's WinUI 3](https://docs.microsoft.com/en-us/windows/apps/winui/winui3/). WinUI 3 is Microsoft's latest native UI component.

### Tutorials and guides

* [Microsoft's Get Started with Win32 and C++](https://docs.microsoft.com/en-us/windows/win32/learnwin32/learn-to-program-for-windows)
* [Microsoft's Build desktop Windows apps using the Win32 API](https://docs.microsoft.com/en-us/windows/win32/)
* [Microsoft's Modernize Your Desktop Apps](https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/). Contains advice and examples on applying the latest Windows 11 UI features to native Windows apps, including Win32 ones.
* [theForger's Win32 API Programming Tutorial](http://www.winprog.org/tutorial/). The tutorials are old, but still useful. Tutorial source code is available on that site as a zip, and I've [also got a repo of it](https://github.com/yottaawesome/forger-win32-tutorial).
* [ZetCode's Windows API tutorial](https://zetcode.com/gui/winapi/)
