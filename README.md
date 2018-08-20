# Mini-Syllabus for Development on Apple Devices

![Swift Logo](https://i.imgur.com/vNMKZKh.png)

### Table of Contents

-   [Mini\-Syllabus for Development on Apple Devices](#mini-syllabus-for-development-on-apple-devices)
    -   [Swift Core Libraries](#swift-core-libraries)
        -   [Foundation](#foundation)
        -   [libdispatch](#libdispatch)
        -   [XCTest](#xctest)
-   [General Links](#general-links)
    -   [Package managers](#package-managers)
    -   [Tools](#tools)
    -   [List to read at glance:](#list-to-read-at-glance)
        -   [Official References](#official-references)
        -   [Playgrounds](#playgrounds)
    -   [Open sourse (client\-server) projects for examples](#open-sourse-client-server-projects-for-examples)
    -   [UI Kit](#ui-kit)
    -   [Debuggers](#debuggers)
-   [FAQ](#faq)
    -   [1. Why Flipper better, then standart debugger?](#1-why-flipper-better-then-standart-debugger)
    -   [2. What is Cocoa?](#2-what-is-cocoa)
-   [Authors](#authors)
    -   [Ivan Istomin](#-ivan-istomin)
    -   [Ilya Gulkov](#-ilya-gulkov)

---

## Swift Core Libraries

The Swift Core Libraries project provides higher-level functionality than the Swift standard library. These libraries provide powerful tools that developers can depend upon across all the platforms that Swift supports. The Core Libraries have a goal of providing stable and useful features in the following key areas:

-   Commonly needed types, including data, URLs, character sets, and specialized collections
-   Unit testing
-   Networking primitives
-   Scheduling and execution of work, including threads, queues, and notifications
-   Persistence, including property lists, archives, JSON parsing, and XML parsing
-   Support for dates, times, and calendrical calculations
-   Abstraction of OS-specific behavior
-   Interaction with the file system
-   Internationalization, including date and number formatting and language-specific resources
-   User preferences

Writing code that provides all of this functionality from scratch would be an enormous undertaking. Therefore, we’ve decided to bootstrap this project by taking advantage of great work that has already been done in these areas. Specifically, we will reuse the API and as much implementation as is possible from three existing libraries: **Foundation**, **libdispatch**, and **XCTest**.

---

### Foundation

The Foundation framework defines a base layer of functionality that is required for almost all applications. It provides primitive classes and introduces several paradigms that define functionality not provided by the language or runtime. It is designed with these goals in mind:

-   Provide a small set of basic utility classes.
-   Make software development easier by introducing consistent conventions.
-   Support internationalization and localization, to make software accessible to users around the world.
-   Provide a level of OS independence, to enhance portability.

More information about the Foundation framework in general is available [from Apple’s documentation](https://developer.apple.com/reference/foundation). The Swift.org version of Foundation makes use of many of the same underlying libraries (e.g. ICU and CoreFoundation) as Apple’s implementation, but has been built to be completely independent of the Objective-C runtime. Because of this, it is a substantial reimplementation of the same API, using pure Swift code layered on top of these common underlying libraries. Much more information about this work is available on our [GitHub project page](http://www.github.com/apple/swift-corelibs-foundation).

---

### libdispatch

Grand Central Dispatch (GCD or libdispatch) provides comprehensive support for concurrent code execution on multicore hardware.

libdispatch is currently available on all Darwin platforms. This project aims to make a modern version of libdispatch available on all other Swift platforms. To do this, we will implement as much of the portable subset of the API as possible, using the existing open source C implementation.

More information about libdispatch for Linux is available on our [GitHub project page](http://www.github.com/apple/swift-corelibs-libdispatch).

---

### XCTest

The XCTest library is designed to provide a common framework for writing unit tests in Swift, for Swift packages and applications.

This version of XCTest uses the same API as the XCTest you are familiar with from Xcode. Our goal is to enable your project’s tests to run on all Swift platforms without having to rewrite them.

More information about XCTest on Linux is available on our [GitHub project page](http://www.github.com/apple/swift-corelibs-xctest).

---

# General Links

-   [Documentation Archive](https://developer.apple.com/library/archive/navigation/)
-   [Apple Developer Documentation](https://developer.apple.com/documentation)
-   [Swift.org main web-site](https://swift.org/)
-   [Awesome Swift](https://github.com/matteocrippa/awesome-swift)
-   [Awesome macOS](https://github.com/iCHAIT/awesome-macOS)
-   [Objective-C Cheat Sheet](https://github.com/iwasrobbed/Objective-C-CheatSheet)
-   [Swift 3+ Cheat Sheet](https://github.com/iwasrobbed/Swift-CheatSheet)
-   [SwiftDoc](https://swiftdoc.org/)

---

## Package managers

1. [Carthage](https://github.com/Carthage/Carthage)
2. [CocoaPods](https://cocoapods.org/)

> Advantages of CocoaPods:
>
> 1. Really easy to use
> 2. Biggest DB of packages
> 3. Really many projects use it

---

## Tools

1. [Xcode Help](https://help.apple.com/xcode/mac/10.0/)
2. [Sparkle](https://sparkle-project.org/)

---

## List to read at glance:

0. [Objective-C Crash Course](https://mega.nz/#!ZGY3BCZL!Ykgx9fgVFnVYYK3Qw78FBOFKzNPqkPKaBBekMDCPFLY)
   0.5. [From C++ to Objective-C](https://mega.nz/#!YK5igC4I!gLWUBNb01LWbO9Qc6nrHk90aUg18MfAT2_3D1ifqeq0)
1. [Learn X in Y minutes](https://learnxinyminutes.com/docs/swift/)
1. [Algorithms and data structures in Swift, with explanations!](https://github.com/raywenderlich/swift-algorithm-club)
1. [macOS Development Tutorials](https://www.raywenderlich.com/category/macos)
1. [Mini mind-map handbook](https://learn-anything.xyz/programming/programming-languages/objective-c)

---

### Official References

1. [Language Guide](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)
2. [Language Reference](https://docs.swift.org/swift-book/ReferenceManual/AboutTheLanguageReference.html)

---

### Playgrounds

1. [A Swift Tour Playground](https://docs.swift.org/swift-book/GuidedTour/GuidedTour.html)
2. ~~[Crustacean.playground](https://developer.apple.com/sample-code/wwdc/2015/downloads/Crustacean.zip)~~
3. [Using JSON with Custom Types](https://developer.apple.com/documentation/foundation/archives_and_serialization/using_json_with_custom_types)
4. [A collection of useful tips for the Swift language in Playground form](https://github.com/vincent-pradeilles/swift-tips)
5. [Playground demonstrating the new features in in Swift 4.2](https://github.com/ole/whats-new-in-swift-4-2)

---

## Open sourse (client-server) projects for examples

Coming soon...

---

## UI Kit

-   [Element](https://github.com/eonist/Element) — Programmatic UI for macOS
    -   [Stash](https://github.com/futurelab/stash) — Simple example app made with Element

---

## Debuggers

-   [LLDB debugger](https://github.com/apple/swift-lldb)
-   [Flipper](https://fbflipper.com/)

---

# FAQ

## 1. Why [Flipper](https://fbflipper.com/) better, then standart debugger?

> With Sonar being built as a standalone app, we can do more things, like handling adb connections and supporting iOS, which wasn't easily achievable with stetho.
>
> This is why we built Sonar. We wanted to create a platform that gives us all the flexibility we need to build more advanced features and support for iOS. One of Sonar's core concept is it's extensibility using plugins.

## 2. What is Cocoa?

> It's Apple's native object-oriented application programming interface (API) for their operating system macOS.

For iOS, tvOS, and watchOS, a similar API exists, named Cocoa Touch, which includes gesture recognition, animation, and a different set of graphical control elements. It is used in applications for Apple devices such as iPhone, iPad, iPod touch, Apple TV, and Apple Watch.

Cocoa consists of the Foundation Kit, Application Kit, and Core Data frameworks, as included by the Cocoa.h header file, and the libraries and frameworks included by those, such as the C standard library and the Objective-C runtime.

---

# Authors

### ![Ivan Istomin](https://png.icons8.com/cotton/50/000000/pills.png) **Ivan Istomin**

### ![Ilya Gulkov](https://png.icons8.com/cotton/50/000000/hand-with-a-pill.png) **Ilya Gulkov**
