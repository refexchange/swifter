### What is Swift?

>Swift is an innovative new programming language for Cocoa and Cocoa Touch. Writing code is interactive and fun, the syntax is concise yet expressive, and apps run lightning-fast. Swift is ready for your next iOS and OS X project — or for addition into your current app — because Swift code works side-by-side with Objective-C.

### What is Swifter?

Tiny http server engine written in Swift ( https://developer.apple.com/swift/ ) programming language.

![Platform](https://img.shields.io/badge/Platform-Linux%20&%20OSX-4BC51D.svg?style=flat)
![Swift](https://img.shields.io/badge/Swift-2.2-4BC51D.svg?style=flat)
![Protocols](https://img.shields.io/badge/Protocols-HTTP%201.1%20&%20WebSockets-4BC51D.svg?style=flat)
[![CocoaPods](https://img.shields.io/cocoapods/v/Swifter.svg?style=flat)]()

### How to start?
```swift
let server = HttpServer()
server["/hello"] = { .OK(.HTML("You asked for " + $0.url)) }
server.start()
```
### How to share files?
```swift
let server = HttpServer()
server["/home/:path"] = HttpHandlers.directory("~/")
server.start()
```
### How to redirect?
```swift
let server = HttpServer()
server["/redirect"] = { request in
  return .MovedPermanently("http://www.google.com")
}
server.start()
```
### CocoaPods? Yes.
```
use_frameworks!
pod 'Swifter', '~> 1.0.9'
```

### Carthage? Also yes.

```
github "glock45/swifter" == 1.0.9
```
