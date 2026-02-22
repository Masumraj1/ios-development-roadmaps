# iOS Development A to Z সম্পূর্ণ গাইড (বাংলা)
## Swift | UIKit | SwiftUI

iOS Development হলো Apple-এর iPhone, iPad, iPod Touch-এর জন্য অ্যাপ্লিকেশন তৈরি করার প্রক্রিয়া। Swift হলো Apple-এর আধুনিক প্রোগ্রামিং ভাষা। UIKit হলো ঐতিহ্যবাহী UI ফ্রেমওয়ার্ক এবং SwiftUI হলো Apple-এর আধুনিক ডিক্লারেটিভ UI ফ্রেমওয়ার্ক।

---

## বিষয়সূচি

### প্রথম ভাগ – Swift ভাষার মূল বিষয়
1. [iOS পরিচিতি](#ios-পরিচিতি)
2. [পরিবেশ সেটআপ](#পরিবেশ-সেটআপ)
3. [Swift মূল বিষয়](#swift-মূল-বিষয়)
4. [অপশনাল (Optional)](#অপশনাল)
5. [ক্লোজার (Closure)](#ক্লোজার)
6. [প্রোটোকল ও এক্সটেনশন](#প্রোটোকল-ও-এক্সটেনশন)
7. [Error Handling](#error-handling)
8. [Concurrency (async/await)](#concurrency)

### দ্বিতীয় ভাগ – UIKit (ঐতিহ্যবাহী পদ্ধতি)
9. [UIKit পরিচিতি](#uikit-পরিচিতি)
10. [প্রথম UIKit প্রজেক্ট](#প্রথম-uikit-প্রজেক্ট)
11. [ViewController লাইফসাইকেল](#viewcontroller-লাইফসাইকেল)
12. [Storyboard ও Xib](#storyboard-ও-xib)
13. [Auto Layout ও Constraints](#auto-layout-ও-constraints)
14. [UIKit উইজেট সমূহ](#uikit-উইজেট-সমূহ)
15. [TableView](#tableview)
16. [CollectionView](#collectionview)
17. [Navigation ও Tab Bar](#navigation-ও-tab-bar)
18. [Alert ও ActionSheet](#alert-ও-actionsheet)
19. [Gesture Recognizer](#gesture-recognizer)
20. [UIKit অ্যানিমেশন](#uikit-অ্যানিমেশন)

### তৃতীয় ভাগ – SwiftUI (আধুনিক পদ্ধতি)
21. [SwiftUI পরিচিতি](#swiftui-পরিচিতি)
22. [SwiftUI View](#swiftui-view)
23. [SwiftUI লেআউট](#swiftui-লেআউট)
24. [SwiftUI উইজেট](#swiftui-উইজেট)
25. [State ও Binding](#state-ও-binding)
26. [List ও ForEach](#list-ও-foreach)
27. [SwiftUI Navigation](#swiftui-navigation)
28. [SwiftUI অ্যানিমেশন](#swiftui-অ্যানিমেশন)
29. [SwiftUI Form](#swiftui-form)

### চতুর্থ ভাগ – Architecture ও ডেটা
30. [MVVM আর্কিটেকচার](#mvvm-আর্কিটেকচার)
31. [Combine Framework](#combine-framework)
32. [Core Data](#core-data)
33. [URLSession ও Networking](#urlsession-ও-networking)
34. [JSON Codable](#json-codable)
35. [UserDefaults ও Keychain](#userdefaults-ও-keychain)
36. [Dependency Injection](#dependency-injection)

### পঞ্চম ভাগ – উন্নত বিষয়
37. [Firebase ইন্টিগ্রেশন](#firebase-ইন্টিগ্রেশন)
38. [Push Notification](#push-notification)
39. [Camera ও Photo Library](#camera-ও-photo-library)
40. [MapKit ও Location](#mapkit-ও-location)
41. [In-App Purchase](#in-app-purchase)
42. [Widget Extension](#widget-extension)
43. [টেস্টিং](#টেস্টিং)
44. [App Store প্রকাশ](#app-store-প্রকাশ)
45. [সম্পূর্ণ প্রজেক্ট উদাহরণ](#সম্পূর্ণ-প্রজেক্ট-উদাহরণ)

---

## iOS পরিচিতি

### iOS কী?
iOS হলো Apple-এর iPhone ও iPad-এর অপারেটিং সিস্টেম। বিশ্বের দ্বিতীয় বৃহত্তম মোবাইল OS, কিন্তু সবচেয়ে লাভজনক অ্যাপ মার্কেট।

### iOS ভার্সন ইতিহাস (সংক্ষেপ)

| ভার্সন | নতুন বৈশিষ্ট্য | বছর |
|--------|---------------|-----|
| iOS 17 | StandBy, Interactive Widgets | 2023 |
| iOS 16 | Lock Screen Customization | 2022 |
| iOS 15 | Focus Mode, SharePlay | 2021 |
| iOS 14 | App Library, Widgets | 2020 |
| iOS 13 | Dark Mode, SwiftUI | 2019 |

### UIKit বনাম SwiftUI

| বৈশিষ্ট্য | UIKit | SwiftUI |
|---------|-------|---------|
| প্রকৃতি | Imperative (কীভাবে) | Declarative (কী) |
| প্রবর্তন | 2008 | 2019 (iOS 13+) |
| UI সংজ্ঞা | Storyboard/Xib/কোড | Swift কোড |
| Xcode Preview | সীমিত | সম্পূর্ণ |
| পুরনো প্রজেক্ট | UIKit | SwiftUI |
| শেখা | তুলনামূলক জটিল | সহজ |

### iOS ডেভেলপমেন্ট স্ট্যাক
```
┌─────────────────────────────────────────┐
│         আপনার অ্যাপ (Swift কোড)         │
├─────────────────────────────────────────┤
│    SwiftUI / UIKit (UI Framework)       │
├─────────────────────────────────────────┤
│   Foundation / AVFoundation / MapKit    │
│   Core Data / Core Location / StoreKit  │
├─────────────────────────────────────────┤
│           iOS Runtime (XNU Kernel)      │
└─────────────────────────────────────────┘
```

---

## পরিবেশ সেটআপ

### প্রয়োজনীয়তা
- **Mac কম্পিউটার** (iOS ডেভেলপমেন্টের জন্য অপরিহার্য)
- **Xcode** (Apple-এর অফিসিয়াল IDE)
- **Apple Developer Account** (টেস্ট ও প্রকাশের জন্য)

### Xcode ইনস্টল করুন
```bash
# App Store থেকে ইনস্টল করুন (সহজতম পদ্ধতি)
# অথবা Apple Developer সাইট থেকে

# Xcode Command Line Tools
xcode-select --install

# Xcode ভার্সন যাচাই
xcodebuild -version
swift --version
```

### CocoaPods (ডিপেন্ডেন্সি ম্যানেজার)
```bash
# CocoaPods ইনস্টল
sudo gem install cocoapods

# প্রজেক্টে initialize
pod init

# Podfile সম্পাদনা করুন, তারপর
pod install

# এরপর .xcworkspace ফাইল খুলুন
open MyApp.xcworkspace
```

### Swift Package Manager (SPM) - আধুনিক পদ্ধতি
```
Xcode → File → Add Package Dependencies
URL: https://github.com/author/package
```

### Simulator ব্যবহার
```bash
# Simulator থেকে অ্যাপ চালান
# Xcode: Product → Run (⌘+R)

# xcrun দিয়ে Simulator খুলুন
xcrun simctl list devices
xcrun simctl boot "iPhone 15"
open -a Simulator
```

---

## Swift মূল বিষয়

### চলক ও ধ্রুবক
```swift
// var – পরিবর্তনযোগ্য
var name = "করিম"
var age = 25
var price = 120.50

// let – অপরিবর্তনীয় (সুপারিশকৃত)
let appName = "বাংলা বাজার"
let pi = 3.14159

// টাইপ অ্যানোটেশন
var score: Int = 0
var message: String = ""
var isLoggedIn: Bool = false
var items: [String] = []
var userInfo: [String: Any] = [:]
```

### ডেটা টাইপ
```swift
// মৌলিক টাইপ
let intValue: Int = 42
let doubleValue: Double = 3.14
let floatValue: Float = 2.5
let boolValue: Bool = true
let stringValue: String = "স্বাগতম"
let charValue: Character = "ক"

// টাইপ রূপান্তর
let number = 42
let text = String(number)        // "42"
let num = Int("42") ?? 0         // 42 (Optional)
let dbl = Double(number)         // 42.0

// String Interpolation
let greeting = "আমার নাম \(name) এবং বয়স \(age)"
let multiLine = """
    এটি
    একটি
    বহুলাইন স্ট্রিং
    """
```

### Collection টাইপ
```swift
// Array
var fruits = ["আম", "কলা", "লিচু"]
fruits.append("জাম")
fruits.insert("পেয়ারা", at: 0)
fruits.remove(at: 1)
let count = fruits.count
let first = fruits.first          // Optional<String>
let sorted = fruits.sorted()

// Dictionary
var prices: [String: Double] = ["আম": 120, "কলা": 30, "লিচু": 80]
prices["পেয়ারা"] = 60
let mangoPrice = prices["আম"]     // Optional<Double>
let keys = Array(prices.keys)
let values = Array(prices.values)

// Set
var uniqueTags: Set<String> = ["swift", "ios", "apple"]
uniqueTags.insert("xcode")
let hasSwift = uniqueTags.contains("swift")

// Tuple
let coordinate = (23.8103, 90.4125)
let user = (name: "করিম", age: 25, email: "karim@email.com")
print(user.name)  // করিম
let (lat, lng) = coordinate
```

### নিয়ন্ত্রণ প্রবাহ
```swift
// if-else
if age >= 18 {
    print("প্রাপ্তবয়স্ক")
} else if age >= 13 {
    print("কিশোর")
} else {
    print("শিশু")
}

// Ternary
let status = age >= 18 ? "প্রাপ্তবয়স্ক" : "অপ্রাপ্তবয়স্ক"

// switch
switch score {
case 90...100:
    print("A+")
case 80..<90:
    print("A")
case 70..<80:
    print("B")
case let x where x < 0:
    print("অবৈধ স্কোর: \(x)")
default:
    print("ফেল")
}

// for-in
for fruit in fruits {
    print(fruit)
}

for (index, fruit) in fruits.enumerated() {
    print("\(index): \(fruit)")
}

for i in 0..<10 { print(i) }
for i in stride(from: 0, to: 100, by: 10) { print(i) }

// while
var count = 0
while count < 5 {
    count += 1
}

// guard – early exit
func process(name: String?) {
    guard let unwrapped = name, !unwrapped.isEmpty else {
        print("নাম নেই")
        return
    }
    print("নাম: \(unwrapped)")
}
```

### ফাংশন
```swift
// সাধারণ ফাংশন
func greet(name: String) -> String {
    return "স্বাগতম, \(name)!"
}

// একাধিক প্যারামিটার
func calculateArea(width: Double, height: Double) -> Double {
    return width * height
}
let area = calculateArea(width: 10, height: 5)

// লেবেল ও প্যারামিটার নাম আলাদা
func add(_ a: Int, to b: Int) -> Int {
    return a + b
}
let sum = add(3, to: 5)

// Default প্যারামিটার
func createUser(name: String, age: Int = 0, role: String = "user") -> String {
    return "\(name) (\(age)) - \(role)"
}
createUser(name: "করিম")
createUser(name: "সুমাইয়া", age: 25, role: "admin")

// একাধিক রিটার্ন (Tuple)
func minMax(array: [Int]) -> (min: Int, max: Int)? {
    guard !array.isEmpty else { return nil }
    return (array.min()!, array.max()!)
}
if let result = minMax(array: [3, 1, 4, 1, 5]) {
    print("সর্বনিম্ন: \(result.min), সর্বোচ্চ: \(result.max)")
}

// Variadic প্যারামিটার
func sum(_ numbers: Int...) -> Int {
    numbers.reduce(0, +)
}
sum(1, 2, 3, 4, 5)

// inout – মূল মান পরিবর্তন
func swap(_ a: inout Int, _ b: inout Int) {
    let temp = a; a = b; b = temp
}
var x = 10, y = 20
swap(&x, &y)
```

### Class, Struct, Enum
```swift
// Struct – মান টাইপ (Value Type), কপি হয়
struct Product {
    var id: Int
    var name: String
    var price: Double
    var category: String

    // কম্পিউটেড প্রপার্টি
    var formattedPrice: String {
        return "৳\(String(format: "%.2f", price))"
    }

    // mutating মেথড – struct-এ self পরিবর্তন করে
    mutating func applyDiscount(_ percent: Double) {
        price *= (1 - percent / 100)
    }

    // static মেথড
    static func createSample() -> Product {
        return Product(id: 1, name: "আম", price: 120, category: "ফল")
    }
}

// Class – রেফারেন্স টাইপ (Reference Type), শেয়ার হয়
class ShoppingCart {
    var items: [Product] = []
    weak var delegate: CartDelegate?  // weak – strong cycle এড়াতে

    var total: Double {
        items.reduce(0) { $0 + $1.price }
    }

    func addItem(_ product: Product) {
        items.append(product)
        delegate?.cartDidUpdate(self)
    }

    func removeItem(at index: Int) {
        guard index < items.count else { return }
        items.remove(at: index)
    }

    // Deinitializer
    deinit {
        print("ShoppingCart মুক্ত হচ্ছে")
    }
}

// Enum
enum OrderStatus: String, CaseIterable {
    case pending = "অপেক্ষারত"
    case confirmed = "নিশ্চিত"
    case processing = "প্রক্রিয়াধীন"
    case shipped = "প্রেরিত"
    case delivered = "বিতরিত"
    case cancelled = "বাতিল"

    var isActive: Bool {
        self != .cancelled && self != .delivered
    }

    var emoji: String {
        switch self {
        case .pending: return "⏳"
        case .confirmed: return "✅"
        case .processing: return "⚙️"
        case .shipped: return "📦"
        case .delivered: return "🎉"
        case .cancelled: return "❌"
        }
    }
}

// Enum with Associated Values
enum NetworkError: Error {
    case noInternet
    case timeout
    case serverError(code: Int, message: String)
    case decodingError(Error)
}

// Result টাইপ
func fetchData() -> Result<[Product], NetworkError> {
    // সফল হলে
    return .success([Product.createSample()])
    // ব্যর্থ হলে
    // return .failure(.serverError(code: 500, message: "সার্ভার ত্রুটি"))
}

switch fetchData() {
case .success(let products):
    print("পণ্য পাওয়া গেছে: \(products.count)টি")
case .failure(let error):
    switch error {
    case .noInternet:
        print("ইন্টারনেট নেই")
    case .serverError(let code, let message):
        print("সার্ভার ত্রুটি \(code): \(message)")
    default:
        print("অজানা ত্রুটি")
    }
}
```

---

## অপশনাল

### Optional কী?
Swift-এ কোনো মান না থাকার সম্ভাবনা Optional দিয়ে প্রকাশ করা হয়। `?` দিয়ে ঘোষণা করা হয়।

```swift
var name: String? = "করিম"
var email: String? = nil    // কোনো মান নেই

// Optional Binding – নিরাপদ আনর্যাপিং
if let unwrappedName = name {
    print("নাম: \(unwrappedName)")
} else {
    print("নাম নেই")
}

// guard let – early exit
func sendEmail(to email: String?) {
    guard let email = email, email.contains("@") else {
        print("অবৈধ ইমেইল")
        return
    }
    print("ইমেইল পাঠানো হচ্ছে: \(email)")
}

// Nil Coalescing – ডিফল্ট মান
let displayName = name ?? "অতিথি"

// Optional Chaining
struct Address {
    var city: String
}
struct Person {
    var address: Address?
}

let person = Person(address: Address(city: "ঢাকা"))
let city = person.address?.city    // Optional("ঢাকা")
let cityName = person.address?.city ?? "অজানা"

// Forced Unwrapping (এড়িয়ে চলুন)
// let forcedName = name!  // nil হলে crash!

// Optional Map
let upperName = name.map { $0.uppercased() }

// if let শর্টহ্যান্ড (Swift 5.7+)
if let name { print("নাম: \(name)") }

// Multiple Optional Binding
if let name = name, let email = email {
    print("\(name): \(email)")
}
```

---

## ক্লোজার

### Closure কী?
Closure হলো Swift-এর প্রথম শ্রেণির ফাংশন। এটি Swift-এর অন্যতম শক্তিশালী বৈশিষ্ট্য।

```swift
// সাধারণ Closure
let greet = { (name: String) -> String in
    return "স্বাগতম, \(name)!"
}
print(greet("করিম"))

// Trailing Closure সিনট্যাক্স
let numbers = [5, 3, 1, 4, 2]
let sorted = numbers.sorted { $0 < $1 }
let sorted2 = numbers.sorted(by: <)

// উচ্চ-ক্রম ফাংশন
let products = [
    Product(id: 1, name: "আম", price: 120, category: "ফল"),
    Product(id: 2, name: "চাল", price: 60, category: "শস্য"),
    Product(id: 3, name: "কলা", price: 30, category: "ফল"),
]

// map – রূপান্তর
let names = products.map { $0.name }              // ["আম", "চাল", "কলা"]
let prices = products.map(\.price)                // [120.0, 60.0, 30.0]

// filter – ছাঁকন
let fruits = products.filter { $0.category == "ফল" }

// reduce – একত্রিত
let totalPrice = products.reduce(0) { $0 + $1.price }

// compactMap – nil বাদ দেওয়া
let optionalNames: [String?] = ["আম", nil, "কলা", nil]
let validNames = optionalNames.compactMap { $0 }  // ["আম", "কলা"]

// flatMap
let nested = [[1, 2], [3, 4], [5, 6]]
let flat = nested.flatMap { $0 }  // [1, 2, 3, 4, 5, 6]

// Escaping Closure
class NetworkManager {
    func fetchData(completion: @escaping (Result<[Product], Error>) -> Void) {
        DispatchQueue.global().async {
            // নেটওয়ার্ক কল
            let products = [Product.createSample()]
            DispatchQueue.main.async {
                completion(.success(products))
            }
        }
    }
}

// Capture List – মেমোরি লিক এড়ানো
class ViewController: UIViewController {
    var networkManager = NetworkManager()

    func loadData() {
        // [weak self] – strong reference cycle এড়ায়
        networkManager.fetchData { [weak self] result in
            guard let self = self else { return }
            switch result {
            case .success(let products): self.updateUI(products)
            case .failure(let error): self.showError(error)
            }
        }
    }
}
```

---

## প্রোটোকল ও এক্সটেনশন

### Protocol
```swift
// Protocol সংজ্ঞা
protocol Describable {
    var description: String { get }
    func describe() -> String
}

protocol Priceable {
    var price: Double { get set }
    func applyDiscount(_ percent: Double) -> Double
}

// Protocol মেথডে default implementation (Extension দিয়ে)
extension Describable {
    func describe() -> String {
        return "বিবরণ: \(description)"
    }
}

// Protocol গ্রহণ
struct Book: Describable, Priceable {
    var title: String
    var price: Double

    var description: String {
        return "\(title) - ৳\(price)"
    }

    func applyDiscount(_ percent: Double) -> Double {
        return price * (1 - percent / 100)
    }
}

// Protocol as Type
func printDescription(_ item: Describable) {
    print(item.describe())
}

// Delegate Pattern
protocol CartDelegate: AnyObject {
    func cartDidUpdate(_ cart: ShoppingCart)
    func cartDidEmpty(_ cart: ShoppingCart)
}

// Codable Protocol – JSON এনকোডিং/ডিকোডিং
struct User: Codable {
    let id: Int
    let name: String
    let email: String

    // কাস্টম কী নাম
    enum CodingKeys: String, CodingKey {
        case id
        case name = "full_name"
        case email
    }
}

// Comparable
struct Product: Comparable {
    var name: String
    var price: Double

    static func < (lhs: Product, rhs: Product) -> Bool {
        return lhs.price < rhs.price
    }
}
```

### Extension
```swift
// String Extension
extension String {
    var isValidEmail: Bool {
        let pattern = "[A-Z0-9a-z._%+-]+@[A-Za-z0-9.-]+\\.[A-Za-z]{2,}"
        return NSPredicate(format: "SELF MATCHES %@", pattern).evaluate(with: self)
    }

    var isValidBDPhone: Bool {
        let pattern = "^01[3-9]\\d{8}$"
        return NSPredicate(format: "SELF MATCHES %@", pattern).evaluate(with: self)
    }

    func capitalizingFirstLetter() -> String {
        return prefix(1).uppercased() + dropFirst()
    }

    var wordCount: Int {
        components(separatedBy: .whitespacesAndNewlines).filter { !$0.isEmpty }.count
    }

    func localized() -> String {
        return NSLocalizedString(self, comment: "")
    }
}

// Int Extension
extension Int {
    var isEven: Bool { self % 2 == 0 }
    var isOdd: Bool { self % 2 != 0 }

    func times(_ task: () -> Void) {
        for _ in 0..<self { task() }
    }
}
3.times { print("স্বাগতম!") }

// Array Extension
extension Array {
    func chunked(into size: Int) -> [[Element]] {
        stride(from: 0, to: count, by: size).map {
            Array(self[$0..<Swift.min($0 + size, count)])
        }
    }

    subscript(safe index: Int) -> Element? {
        indices.contains(index) ? self[index] : nil
    }
}

// UIColor Extension
extension UIColor {
    static var appPrimary: UIColor { UIColor(named: "AppPrimary") ?? .systemBlue }
    static var appBackground: UIColor { UIColor(named: "AppBackground") ?? .systemBackground }

    convenience init(hex: String) {
        var hexFormatted = hex.trimmingCharacters(in: .whitespacesAndNewlines).uppercased()
        if hexFormatted.hasPrefix("#") { hexFormatted.removeFirst() }
        var rgb: UInt64 = 0
        Scanner(string: hexFormatted).scanHexInt64(&rgb)
        let r = CGFloat((rgb & 0xFF0000) >> 16) / 255
        let g = CGFloat((rgb & 0x00FF00) >> 8) / 255
        let b = CGFloat(rgb & 0x0000FF) / 255
        self.init(red: r, green: g, blue: b, alpha: 1)
    }
}
```

---

## Error Handling

```swift
// Custom Error
enum AppError: LocalizedError {
    case networkUnavailable
    case invalidData
    case unauthorized
    case notFound(id: Int)
    case serverError(code: Int)

    var errorDescription: String? {
        switch self {
        case .networkUnavailable: return "ইন্টারনেট সংযোগ নেই"
        case .invalidData: return "অবৈধ ডেটা"
        case .unauthorized: return "অননুমোদিত অ্যাক্সেস"
        case .notFound(let id): return "আইটেম \(id) পাওয়া যায়নি"
        case .serverError(let code): return "সার্ভার ত্রুটি: \(code)"
        }
    }
}

// throws ফাংশন
func validateUser(name: String, age: Int) throws -> String {
    guard !name.isEmpty else { throw AppError.invalidData }
    guard age >= 0 && age <= 150 else { throw AppError.invalidData }
    return "\(name) (\(age))"
}

// do-catch
do {
    let user = try validateUser(name: "করিম", age: 25)
    print(user)
} catch AppError.invalidData {
    print("ডেটা সঠিক নয়")
} catch AppError.networkUnavailable {
    print("নেটওয়ার্ক সমস্যা")
} catch {
    print("অজানা ত্রুটি: \(error.localizedDescription)")
}

// try? – Optional রিটার্ন
let user = try? validateUser(name: "করিম", age: 25)

// try! – Forced (ক্র্যাশ হতে পারে, এড়িয়ে চলুন)
// let user = try! validateUser(name: "করিম", age: 25)

// rethrows
func perform<T>(operation: () throws -> T) rethrows -> T {
    return try operation()
}
```

---

## Concurrency

### async/await (Swift 5.5+)
```swift
// Async ফাংশন
func fetchProducts() async throws -> [Product] {
    let url = URL(string: "https://api.example.com/products")!
    let (data, response) = try await URLSession.shared.data(from: url)

    guard let httpResponse = response as? HTTPURLResponse, httpResponse.statusCode == 200 else {
        throw AppError.serverError(code: (response as? HTTPURLResponse)?.statusCode ?? 0)
    }

    return try JSONDecoder().decode([Product].self, from: data)
}

// Task দিয়ে কল করা
func loadProducts() {
    Task {
        do {
            let products = try await fetchProducts()
            await MainActor.run {
                // UI আপডেট (Main Thread-এ)
                self.products = products
            }
        } catch {
            print("ত্রুটি: \(error.localizedDescription)")
        }
    }
}

// async let – সমান্তরাল কাজ
func loadDashboard() async throws {
    async let products = fetchProducts()
    async let categories = fetchCategories()
    async let user = fetchCurrentUser()

    let (p, c, u) = try await (products, categories, user)
    updateDashboard(products: p, categories: c, user: u)
}

// Actor – Thread-safe স্টেট
actor DataCache {
    private var cache: [Int: Product] = [:]

    func store(_ product: Product) {
        cache[product.id] = product
    }

    func get(id: Int) -> Product? {
        return cache[id]
    }
}

// @MainActor – Main Thread গ্যারান্টি
@MainActor
class ProductViewModel: ObservableObject {
    @Published var products: [Product] = []
    @Published var isLoading = false
    @Published var error: String?

    func loadProducts() async {
        isLoading = true
        defer { isLoading = false }

        do {
            products = try await fetchProducts()
        } catch {
            self.error = error.localizedDescription
        }
    }
}
```

---

# দ্বিতীয় ভাগ – UIKit

## UIKit পরিচিতি

### UIKit কী?
UIKit হলো iOS-এর মূল UI ফ্রেমওয়ার্ক। 2008 সাল থেকে ব্যবহৃত হচ্ছে। বেশিরভাগ পুরনো প্রজেক্ট UIKit দিয়ে তৈরি।

### UIKit আর্কিটেকচার
```
UIWindow
└── UIViewController (Root)
    └── UIView (Root View)
        ├── UILabel
        ├── UIButton
        ├── UIImageView
        └── UIStackView
            ├── UITextField
            └── UIButton
```

---

## প্রথম UIKit প্রজেক্ট

```swift
// AppDelegate.swift
import UIKit

@main
class AppDelegate: UIResponder, UIApplicationDelegate {
    func application(_ application: UIApplication,
                     didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        return true
    }
}

// SceneDelegate.swift
class SceneDelegate: UIResponder, UIWindowSceneDelegate {
    var window: UIWindow?

    func scene(_ scene: UIScene, willConnectTo session: UISceneSession,
               options connectionOptions: UIScene.ConnectionOptions) {
        guard let windowScene = scene as? UIWindowScene else { return }

        // Storyboard ছাড়া কোডে UI তৈরি
        window = UIWindow(windowScene: windowScene)
        let navController = UINavigationController(rootViewController: HomeViewController())
        window?.rootViewController = navController
        window?.makeKeyAndVisible()
    }
}

// HomeViewController.swift
class HomeViewController: UIViewController {

    // UI উপাদান
    private let titleLabel: UILabel = {
        let label = UILabel()
        label.text = "স্বাগতম iOS-এ!"
        label.font = .systemFont(ofSize: 24, weight: .bold)
        label.textAlignment = .center
        label.translatesAutoresizingMaskIntoConstraints = false
        return label
    }()

    private let actionButton: UIButton = {
        let button = UIButton(type: .system)
        button.setTitle("ক্লিক করুন", for: .normal)
        button.titleLabel?.font = .systemFont(ofSize: 16, weight: .semibold)
        button.backgroundColor = .systemBlue
        button.setTitleColor(.white, for: .normal)
        button.layer.cornerRadius = 12
        button.translatesAutoresizingMaskIntoConstraints = false
        return button
    }()

    override func viewDidLoad() {
        super.viewDidLoad()
        setupUI()
        setupConstraints()
        setupActions()
    }

    private func setupUI() {
        view.backgroundColor = .systemBackground
        title = "হোম"
        view.addSubview(titleLabel)
        view.addSubview(actionButton)
    }

    private func setupConstraints() {
        NSLayoutConstraint.activate([
            titleLabel.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            titleLabel.centerYAnchor.constraint(equalTo: view.centerYAnchor, constant: -50),
            titleLabel.leadingAnchor.constraint(equalTo: view.leadingAnchor, constant: 16),
            titleLabel.trailingAnchor.constraint(equalTo: view.trailingAnchor, constant: -16),

            actionButton.topAnchor.constraint(equalTo: titleLabel.bottomAnchor, constant: 24),
            actionButton.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            actionButton.widthAnchor.constraint(equalToConstant: 200),
            actionButton.heightAnchor.constraint(equalToConstant: 50),
        ])
    }

    private func setupActions() {
        actionButton.addTarget(self, action: #selector(buttonTapped), for: .touchUpInside)
    }

    @objc private func buttonTapped() {
        titleLabel.text = "বাটন চাপা হয়েছে! 🎉"
        UIView.animate(withDuration: 0.3) {
            self.actionButton.alpha = 0.7
        } completion: { _ in
            UIView.animate(withDuration: 0.3) {
                self.actionButton.alpha = 1.0
            }
        }
    }
}
```

---

## ViewController লাইফসাইকেল

```swift
class LifecycleViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // একবার কল হয় – UI সেটআপ, ডেটা লোড শুরু
        print("viewDidLoad")
    }

    override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        // স্ক্রিন দেখানোর আগে – নেভিগেশন বার কনফিগার
        print("viewWillAppear")
    }

    override func viewDidAppear(_ animated: Bool) {
        super.viewDidAppear(animated)
        // স্ক্রিন দেখানো হয়েছে – অ্যানিমেশন শুরু
        print("viewDidAppear")
    }

    override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        // স্ক্রিন যাওয়ার আগে – কাজ সংরক্ষণ
        print("viewWillDisappear")
    }

    override func viewDidDisappear(_ animated: Bool) {
        super.viewDidDisappear(animated)
        // স্ক্রিন চলে গেছে
        print("viewDidDisappear")
    }

    override func viewWillLayoutSubviews() {
        super.viewWillLayoutSubviews()
        // লেআউট পরিবর্তনের আগে
    }

    override func viewDidLayoutSubviews() {
        super.viewDidLayoutSubviews()
        // লেআউট সম্পন্ন – frame ব্যবহার করুন এখানে
    }

    deinit {
        print("ViewController মুক্ত হচ্ছে")
        // Observer সরান, Timer বন্ধ করুন
    }
}
```

---

## Storyboard ও Xib

### Storyboard
```swift
// Storyboard থেকে ViewController লোড
let storyboard = UIStoryboard(name: "Main", bundle: nil)
let vc = storyboard.instantiateViewController(withIdentifier: "DetailVC") as! DetailViewController
vc.productId = 123
navigationController?.pushViewController(vc, animated: true)

// @IBOutlet ও @IBAction সংযোগ
class LoginViewController: UIViewController {

    @IBOutlet weak var emailTextField: UITextField!
    @IBOutlet weak var passwordTextField: UITextField!
    @IBOutlet weak var loginButton: UIButton!
    @IBOutlet weak var loadingIndicator: UIActivityIndicatorView!

    @IBAction func loginTapped(_ sender: UIButton) {
        guard let email = emailTextField.text, !email.isEmpty,
              let password = passwordTextField.text, !password.isEmpty else {
            showAlert(message: "সব তথ্য পূরণ করুন")
            return
        }
        performLogin(email: email, password: password)
    }
}
```

---

## Auto Layout ও Constraints

```swift
// SnapKit ব্যবহার (CocoaPods: pod 'SnapKit')
import SnapKit

class ProductCardView: UIView {
    private let imageView = UIImageView()
    private let nameLabel = UILabel()
    private let priceLabel = UILabel()
    private let addButton = UIButton()

    override init(frame: CGRect) {
        super.init(frame: frame)
        setupUI()
    }

    required init?(coder: NSCoder) { fatalError() }

    private func setupUI() {
        layer.cornerRadius = 12
        layer.shadowColor = UIColor.black.cgColor
        layer.shadowOpacity = 0.1
        layer.shadowRadius = 8
        backgroundColor = .systemBackground

        addSubview(imageView)
        addSubview(nameLabel)
        addSubview(priceLabel)
        addSubview(addButton)

        // SnapKit Constraints
        imageView.snp.makeConstraints { make in
            make.top.leading.trailing.equalToSuperview()
            make.height.equalTo(150)
        }

        nameLabel.snp.makeConstraints { make in
            make.top.equalTo(imageView.snp.bottom).offset(8)
            make.leading.trailing.equalToSuperview().inset(12)
        }

        priceLabel.snp.makeConstraints { make in
            make.top.equalTo(nameLabel.snp.bottom).offset(4)
            make.leading.equalToSuperview().inset(12)
        }

        addButton.snp.makeConstraints { make in
            make.trailing.equalToSuperview().inset(12)
            make.centerY.equalTo(priceLabel)
            make.width.height.equalTo(32)
            make.bottom.equalToSuperview().inset(12)
        }
    }

    func configure(with product: Product) {
        nameLabel.text = product.name
        priceLabel.text = product.formattedPrice
        nameLabel.font = .systemFont(ofSize: 14, weight: .semibold)
        priceLabel.textColor = .systemGreen
        imageView.contentMode = .scaleAspectFill
        imageView.clipsToBounds = true
        imageView.layer.cornerRadius = 12
        imageView.layer.maskedCorners = [.layerMinXMinYCorner, .layerMaxXMinYCorner]
    }
}
```

---

## UIKit উইজেট সমূহ

```swift
// UILabel
let label = UILabel()
label.text = "পণ্যের নাম"
label.font = UIFont(name: "HindSiliguri-Bold", size: 18) ?? .boldSystemFont(ofSize: 18)
label.textColor = .label
label.numberOfLines = 0  // সীমাহীন লাইন
label.lineBreakMode = .byWordWrapping
label.textAlignment = .left

// UIButton (UIButton.Configuration – iOS 15+)
var config = UIButton.Configuration.filled()
config.title = "কার্টে যোগ করুন"
config.image = UIImage(systemName: "cart.badge.plus")
config.imagePadding = 8
config.cornerStyle = .large
config.baseBackgroundColor = .systemGreen
let button = UIButton(configuration: config)

// UITextField
let textField = UITextField()
textField.placeholder = "ইমেইল লিখুন"
textField.borderStyle = .roundedRect
textField.keyboardType = .emailAddress
textField.autocapitalizationType = .none
textField.returnKeyType = .next
textField.clearButtonMode = .whileEditing
textField.delegate = self

// UIImageView
let imageView = UIImageView()
imageView.contentMode = .scaleAspectFill
imageView.clipsToBounds = true
imageView.layer.cornerRadius = 8
// URLSession দিয়ে ছবি লোড (অথবা SDWebImage/Kingfisher)
imageView.loadImage(from: "https://example.com/image.jpg")

// UIStackView
let stackView = UIStackView(arrangedSubviews: [nameLabel, priceLabel, addButton])
stackView.axis = .vertical          // .horizontal
stackView.spacing = 8
stackView.alignment = .leading      // .center, .trailing, .fill
stackView.distribution = .fill      // .equalSpacing, .fillEqually

// UIScrollView
let scrollView = UIScrollView()
let contentView = UIView()
scrollView.addSubview(contentView)
scrollView.showsVerticalScrollIndicator = false
scrollView.alwaysBounceVertical = true

// UISwitch
let toggle = UISwitch()
toggle.isOn = true
toggle.onTintColor = .systemGreen
toggle.addTarget(self, action: #selector(toggleChanged), for: .valueChanged)

// UISlider
let slider = UISlider()
slider.minimumValue = 0
slider.maximumValue = 10000
slider.value = 5000
slider.tintColor = .systemBlue

// UISegmentedControl
let segment = UISegmentedControl(items: ["সব", "ফল", "সবজি"])
segment.selectedSegmentIndex = 0
segment.addTarget(self, action: #selector(segmentChanged), for: .valueChanged)

// UIDatePicker
let datePicker = UIDatePicker()
datePicker.datePickerMode = .date
datePicker.preferredDatePickerStyle = .wheels
datePicker.locale = Locale(identifier: "bn_BD")

// UIActivityIndicatorView
let spinner = UIActivityIndicatorView(style: .large)
spinner.color = .systemBlue
spinner.hidesWhenStopped = true
spinner.startAnimating()
// spinner.stopAnimating()

// UIProgressView
let progressView = UIProgressView(progressViewStyle: .default)
progressView.progress = 0.7
progressView.tintColor = .systemBlue
```

---

## TableView

### UITableView সেটআপ
```swift
// Cell
class ProductCell: UITableViewCell {
    static let identifier = "ProductCell"

    private let productImageView = UIImageView()
    private let nameLabel = UILabel()
    private let priceLabel = UILabel()
    private let categoryLabel = UILabel()

    override init(style: UITableViewCell.CellStyle, reuseIdentifier: String?) {
        super.init(style: style, reuseIdentifier: reuseIdentifier)
        setupUI()
    }

    required init?(coder: NSCoder) { fatalError() }

    private func setupUI() {
        let stack = UIStackView(arrangedSubviews: [nameLabel, categoryLabel, priceLabel])
        stack.axis = .vertical
        stack.spacing = 4

        contentView.addSubview(productImageView)
        contentView.addSubview(stack)

        productImageView.snp.makeConstraints { make in
            make.leading.equalToSuperview().inset(16)
            make.centerY.equalToSuperview()
            make.width.height.equalTo(60)
        }
        productImageView.layer.cornerRadius = 8
        productImageView.clipsToBounds = true

        stack.snp.makeConstraints { make in
            make.leading.equalTo(productImageView.snp.trailing).offset(12)
            make.trailing.equalToSuperview().inset(16)
            make.centerY.equalToSuperview()
        }

        nameLabel.font = .systemFont(ofSize: 16, weight: .semibold)
        categoryLabel.font = .systemFont(ofSize: 13)
        categoryLabel.textColor = .secondaryLabel
        priceLabel.font = .systemFont(ofSize: 15, weight: .bold)
        priceLabel.textColor = .systemGreen
    }

    func configure(with product: Product) {
        nameLabel.text = product.name
        categoryLabel.text = product.category
        priceLabel.text = product.formattedPrice
        productImageView.loadImage(from: product.imageUrl)
    }
}

// ViewController
class ProductListViewController: UIViewController {

    private let tableView = UITableView()
    private var products: [Product] = []
    private var filteredProducts: [Product] = []
    private let searchController = UISearchController(searchResultsController: nil)

    override func viewDidLoad() {
        super.viewDidLoad()
        setupTableView()
        setupSearchController()
        loadData()
    }

    private func setupTableView() {
        view.addSubview(tableView)
        tableView.frame = view.bounds
        tableView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        tableView.register(ProductCell.self, forCellReuseIdentifier: ProductCell.identifier)
        tableView.dataSource = self
        tableView.delegate = self
        tableView.rowHeight = UITableView.automaticDimension
        tableView.estimatedRowHeight = 80
        tableView.separatorStyle = .singleLine

        // Refresh Control
        let refreshControl = UIRefreshControl()
        refreshControl.addTarget(self, action: #selector(refreshData), for: .valueChanged)
        tableView.refreshControl = refreshControl
    }

    private func setupSearchController() {
        searchController.searchResultsUpdater = self
        searchController.obscuresBackgroundDuringPresentation = false
        searchController.searchBar.placeholder = "পণ্য খুঁজুন..."
        navigationItem.searchController = searchController
        navigationItem.hidesSearchBarWhenScrolling = false
    }

    private func loadData() {
        Task {
            do {
                products = try await ProductService().getProducts()
                filteredProducts = products
                await MainActor.run { tableView.reloadData() }
            } catch {
                await MainActor.run { showAlert(message: error.localizedDescription) }
            }
        }
    }

    @objc private func refreshData() {
        Task {
            await loadData()
            await MainActor.run { tableView.refreshControl?.endRefreshing() }
        }
    }
}

// DataSource & Delegate
extension ProductListViewController: UITableViewDataSource {
    func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        return filteredProducts.count
    }

    func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: ProductCell.identifier, for: indexPath) as! ProductCell
        cell.configure(with: filteredProducts[indexPath.row])
        return cell
    }

    // Swipe to Delete
    func tableView(_ tableView: UITableView, commit editingStyle: UITableViewCell.EditingStyle, forRowAt indexPath: IndexPath) {
        if editingStyle == .delete {
            filteredProducts.remove(at: indexPath.row)
            tableView.deleteRows(at: [indexPath], with: .fade)
        }
    }
}

extension ProductListViewController: UITableViewDelegate {
    func tableView(_ tableView: UITableView, didSelectRowAt indexPath: IndexPath) {
        tableView.deselectRow(at: indexPath, animated: true)
        let product = filteredProducts[indexPath.row]
        let detailVC = ProductDetailViewController(product: product)
        navigationController?.pushViewController(detailVC, animated: true)
    }

    // Context Menu
    func tableView(_ tableView: UITableView, contextMenuConfigurationForRowAt indexPath: IndexPath, point: CGPoint) -> UIContextMenuConfiguration? {
        let product = filteredProducts[indexPath.row]
        return UIContextMenuConfiguration(identifier: nil, previewProvider: nil) { _ in
            let addToCart = UIAction(title: "কার্টে যোগ", image: UIImage(systemName: "cart.badge.plus")) { _ in
                CartManager.shared.add(product)
            }
            let share = UIAction(title: "শেয়ার", image: UIImage(systemName: "square.and.arrow.up")) { _ in
                self.share(product)
            }
            return UIMenu(children: [addToCart, share])
        }
    }
}

// Search
extension ProductListViewController: UISearchResultsUpdating {
    func updateSearchResults(for searchController: UISearchController) {
        guard let query = searchController.searchBar.text, !query.isEmpty else {
            filteredProducts = products
            tableView.reloadData()
            return
        }
        filteredProducts = products.filter { $0.name.localizedCaseInsensitiveContains(query) }
        tableView.reloadData()
    }
}
```

---

## CollectionView

```swift
// CompositionalLayout – iOS 13+ (শক্তিশালী লেআউট)
class ProductCollectionViewController: UIViewController {

    private var collectionView: UICollectionView!
    private var dataSource: UICollectionViewDiffableDataSource<Section, Product>!

    enum Section { case main }

    override func viewDidLoad() {
        super.viewDidLoad()
        setupCollectionView()
        setupDataSource()
        loadData()
    }

    private func createLayout() -> UICollectionViewLayout {
        // গ্রিড লেআউট
        let itemSize = NSCollectionLayoutSize(widthDimension: .fractionalWidth(0.5), heightDimension: .fractionalHeight(1.0))
        let item = NSCollectionLayoutItem(layoutSize: itemSize)
        item.contentInsets = NSDirectionalEdgeInsets(top: 4, leading: 4, bottom: 4, trailing: 4)

        let groupSize = NSCollectionLayoutSize(widthDimension: .fractionalWidth(1.0), heightDimension: .absolute(200))
        let group = NSCollectionLayoutGroup.horizontal(layoutSize: groupSize, subitems: [item])

        let section = NSCollectionLayoutSection(group: group)
        section.contentInsets = NSDirectionalEdgeInsets(top: 8, leading: 8, bottom: 8, trailing: 8)

        // Header
        let headerSize = NSCollectionLayoutSize(widthDimension: .fractionalWidth(1.0), heightDimension: .absolute(44))
        let header = NSCollectionLayoutBoundarySupplementaryItem(layoutSize: headerSize, elementKind: UICollectionView.elementKindSectionHeader, alignment: .top)
        section.boundarySupplementaryItems = [header]

        return UICollectionViewCompositionalLayout(section: section)
    }

    private func setupCollectionView() {
        collectionView = UICollectionView(frame: view.bounds, collectionViewLayout: createLayout())
        collectionView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        collectionView.backgroundColor = .systemGroupedBackground
        view.addSubview(collectionView)
        collectionView.register(ProductCollectionCell.self, forCellWithReuseIdentifier: "ProductCell")
    }

    private func setupDataSource() {
        // DiffableDataSource
        dataSource = UICollectionViewDiffableDataSource<Section, Product>(collectionView: collectionView) { collectionView, indexPath, product in
            let cell = collectionView.dequeueReusableCell(withReuseIdentifier: "ProductCell", for: indexPath) as! ProductCollectionCell
            cell.configure(with: product)
            return cell
        }
    }

    private func loadData() {
        Task {
            let products = try? await ProductService().getProducts()
            var snapshot = NSDiffableDataSourceSnapshot<Section, Product>()
            snapshot.appendSections([.main])
            snapshot.appendItems(products ?? [])
            await MainActor.run { dataSource.apply(snapshot, animatingDifferences: true) }
        }
    }
}
```

---

## Navigation ও Tab Bar

```swift
// UINavigationController
class AppCoordinator {
    var window: UIWindow

    init(window: UIWindow) {
        self.window = window
    }

    func start() {
        let homeVC = HomeViewController()
        let navController = UINavigationController(rootViewController: homeVC)
        navController.navigationBar.prefersLargeTitles = true

        let tabController = UITabBarController()
        let homeNav = UINavigationController(rootViewController: HomeViewController())
        let searchNav = UINavigationController(rootViewController: SearchViewController())
        let cartNav = UINavigationController(rootViewController: CartViewController())
        let profileNav = UINavigationController(rootViewController: ProfileViewController())

        homeNav.tabBarItem = UITabBarItem(title: "হোম", image: UIImage(systemName: "house"), tag: 0)
        searchNav.tabBarItem = UITabBarItem(title: "খুঁজুন", image: UIImage(systemName: "magnifyingglass"), tag: 1)
        cartNav.tabBarItem = UITabBarItem(title: "কার্ট", image: UIImage(systemName: "cart"), tag: 2)
        profileNav.tabBarItem = UITabBarItem(title: "প্রোফাইল", image: UIImage(systemName: "person"), tag: 3)

        tabController.viewControllers = [homeNav, searchNav, cartNav, profileNav]

        window.rootViewController = tabController
        window.makeKeyAndVisible()
    }
}

// ViewController-এ নেভিগেশন
class HomeViewController: UIViewController {

    // Push
    func openDetail(product: Product) {
        let detailVC = ProductDetailViewController(product: product)
        navigationController?.pushViewController(detailVC, animated: true)
    }

    // Modal Present
    func openFilter() {
        let filterVC = FilterViewController()
        filterVC.modalPresentationStyle = .pageSheet
        if let sheet = filterVC.sheetPresentationController {
            sheet.detents = [.medium(), .large()]
            sheet.prefersGrabberVisible = true
        }
        present(filterVC, animated: true)
    }

    // ডেটা পাঠানো (Protocol/Closure/Notification)
    func openAddProduct() {
        let addVC = AddProductViewController()
        addVC.onProductAdded = { [weak self] product in
            self?.products.insert(product, at: 0)
            self?.tableView.reloadData()
        }
        navigationController?.pushViewController(addVC, animated: true)
    }
}
```

---

## Alert ও ActionSheet

```swift
extension UIViewController {

    // Simple Alert
    func showAlert(title: String = "বিজ্ঞপ্তি", message: String, completion: (() -> Void)? = nil) {
        let alert = UIAlertController(title: title, message: message, preferredStyle: .alert)
        alert.addAction(UIAlertAction(title: "ঠিক আছে", style: .default) { _ in completion?() })
        present(alert, animated: true)
    }

    // Confirmation Alert
    func showConfirmation(title: String, message: String, onConfirm: @escaping () -> Void) {
        let alert = UIAlertController(title: title, message: message, preferredStyle: .alert)
        alert.addAction(UIAlertAction(title: "হ্যাঁ", style: .destructive) { _ in onConfirm() })
        alert.addAction(UIAlertAction(title: "না", style: .cancel))
        present(alert, animated: true)
    }

    // Text Input Alert
    func showInputAlert(title: String, placeholder: String, onSubmit: @escaping (String) -> Void) {
        let alert = UIAlertController(title: title, message: nil, preferredStyle: .alert)
        alert.addTextField { textField in
            textField.placeholder = placeholder
        }
        alert.addAction(UIAlertAction(title: "বাতিল", style: .cancel))
        alert.addAction(UIAlertAction(title: "জমা", style: .default) { _ in
            if let text = alert.textFields?.first?.text, !text.isEmpty {
                onSubmit(text)
            }
        })
        present(alert, animated: true)
    }

    // Action Sheet
    func showActionSheet(title: String, actions: [(String, UIAlertAction.Style, () -> Void)]) {
        let sheet = UIAlertController(title: title, message: nil, preferredStyle: .actionSheet)
        actions.forEach { (title, style, action) in
            sheet.addAction(UIAlertAction(title: title, style: style) { _ in action() })
        }
        sheet.addAction(UIAlertAction(title: "বাতিল", style: .cancel))
        // iPad-এ popover দরকার
        if let popover = sheet.popoverPresentationController {
            popover.sourceView = view
            popover.sourceRect = CGRect(x: view.bounds.midX, y: view.bounds.midY, width: 0, height: 0)
        }
        present(sheet, animated: true)
    }
}

// ব্যবহার
showConfirmation(title: "নিশ্চিত করুন", message: "পণ্যটি মুছবেন?") {
    viewModel.deleteProduct(productId)
}

showActionSheet(title: "ছবি নির্বাচন", actions: [
    ("ক্যামেরা", .default, { self.openCamera() }),
    ("গ্যালারি", .default, { self.openGallery() }),
    ("মুছুন", .destructive, { self.removePhoto() })
])
```

---

## Gesture Recognizer

```swift
class GestureViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        setupGestures()
    }

    private func setupGestures() {
        let tapGesture = UITapGestureRecognizer(target: self, action: #selector(handleTap(_:)))
        tapGesture.numberOfTapsRequired = 1
        view.addGestureRecognizer(tapGesture)

        let doubleTapGesture = UITapGestureRecognizer(target: self, action: #selector(handleDoubleTap))
        doubleTapGesture.numberOfTapsRequired = 2
        view.addGestureRecognizer(doubleTapGesture)

        // Single tap একমাত্র কাজ করবে যখন double tap ব্যর্থ হবে
        tapGesture.require(toFail: doubleTapGesture)

        let longPress = UILongPressGestureRecognizer(target: self, action: #selector(handleLongPress(_:)))
        longPress.minimumPressDuration = 0.5
        view.addGestureRecognizer(longPress)

        let swipeLeft = UISwipeGestureRecognizer(target: self, action: #selector(handleSwipe(_:)))
        swipeLeft.direction = .left
        view.addGestureRecognizer(swipeLeft)

        let pan = UIPanGestureRecognizer(target: self, action: #selector(handlePan(_:)))
        view.addGestureRecognizer(pan)

        let pinch = UIPinchGestureRecognizer(target: self, action: #selector(handlePinch(_:)))
        view.addGestureRecognizer(pinch)
    }

    @objc func handleTap(_ gesture: UITapGestureRecognizer) {
        let location = gesture.location(in: view)
        print("ট্যাপ: \(location)")
    }

    @objc func handleDoubleTap() { print("ডাবল ট্যাপ") }

    @objc func handleLongPress(_ gesture: UILongPressGestureRecognizer) {
        if gesture.state == .began { print("দীর্ঘ প্রেস শুরু") }
    }

    @objc func handleSwipe(_ gesture: UISwipeGestureRecognizer) {
        print("সোয়াইপ: \(gesture.direction)")
    }

    private var startCenter = CGPoint.zero

    @objc func handlePan(_ gesture: UIPanGestureRecognizer) {
        let translation = gesture.translation(in: view)
        if gesture.state == .began { startCenter = gesture.view?.center ?? .zero }
        gesture.view?.center = CGPoint(x: startCenter.x + translation.x, y: startCenter.y + translation.y)
    }

    @objc func handlePinch(_ gesture: UIPinchGestureRecognizer) {
        gesture.view?.transform = gesture.view!.transform.scaledBy(x: gesture.scale, y: gesture.scale)
        gesture.scale = 1.0
    }
}
```

---

## UIKit অ্যানিমেশন

```swift
// সাধারণ অ্যানিমেশন
UIView.animate(withDuration: 0.3) {
    self.view.alpha = 0.5
    self.button.transform = CGAffineTransform(scaleX: 1.1, y: 1.1)
}

// Spring অ্যানিমেশন
UIView.animate(withDuration: 0.6, delay: 0, usingSpringWithDamping: 0.5, initialSpringVelocity: 0.5) {
    self.card.transform = .identity
}

// Keyframe অ্যানিমেশন
UIView.animateKeyframes(withDuration: 1.0, delay: 0) {
    UIView.addKeyframe(withRelativeStartTime: 0, relativeDuration: 0.3) {
        self.view.backgroundColor = .systemBlue
    }
    UIView.addKeyframe(withRelativeStartTime: 0.3, relativeDuration: 0.4) {
        self.titleLabel.alpha = 1.0
    }
    UIView.addKeyframe(withRelativeStartTime: 0.7, relativeDuration: 0.3) {
        self.button.transform = .identity
    }
}

// Transition অ্যানিমেশন
UIView.transition(with: containerView, duration: 0.4, options: .transitionFlipFromRight) {
    self.imageView.image = newImage
}

// CALayer অ্যানিমেশন
let pulseAnimation = CAKeyframeAnimation(keyPath: "transform.scale")
pulseAnimation.values = [1.0, 1.2, 0.9, 1.1, 1.0]
pulseAnimation.duration = 0.5
button.layer.add(pulseAnimation, forKey: "pulse")
```

---

# তৃতীয় ভাগ – SwiftUI

## SwiftUI পরিচিতি

### SwiftUI কী?
SwiftUI হলো Apple-এর ডিক্লারেটিভ UI ফ্রেমওয়ার্ক (iOS 13+)। এটি দিয়ে একই কোড দিয়ে iPhone, iPad, Mac, Apple Watch, Apple TV-তে UI তৈরি করা যায়।

### SwiftUI বনাম UIKit
```swift
// UIKit পদ্ধতি
let label = UILabel()
label.text = "স্বাগতম"
label.textColor = .systemBlue
view.addSubview(label)

// SwiftUI পদ্ধতি – অনেক সহজ!
Text("স্বাগতম")
    .foregroundColor(.blue)
```

---

## SwiftUI View

```swift
import SwiftUI

// সহজ View
struct GreetingView: View {
    var name: String

    var body: some View {
        Text("স্বাগতম, \(name)!")
            .font(.title)
            .fontWeight(.bold)
            .foregroundColor(.blue)
    }
}

// কাস্টম Card View
struct ProductCardView: View {
    let product: Product
    let onAddToCart: () -> Void
    let onFavorite: () -> Void

    var body: some View {
        VStack(alignment: .leading, spacing: 0) {
            // ছবি
            AsyncImage(url: URL(string: product.imageUrl)) { image in
                image.resizable().aspectRatio(contentMode: .fill)
            } placeholder: {
                Rectangle().fill(Color.gray.opacity(0.2))
                    .overlay(Image(systemName: "photo").font(.largeTitle).foregroundColor(.gray))
            }
            .frame(height: 160)
            .clipped()

            // তথ্য
            VStack(alignment: .leading, spacing: 6) {
                Text(product.name)
                    .font(.system(size: 16, weight: .semibold))
                    .lineLimit(1)

                Text(product.category)
                    .font(.caption)
                    .foregroundColor(.secondary)

                HStack {
                    Text(product.formattedPrice)
                        .font(.system(size: 15, weight: .bold))
                        .foregroundColor(.green)

                    Spacer()

                    Button(action: onFavorite) {
                        Image(systemName: product.isFavorite ? "heart.fill" : "heart")
                            .foregroundColor(product.isFavorite ? .red : .gray)
                    }

                    Button(action: onAddToCart) {
                        Image(systemName: "cart.badge.plus")
                            .foregroundColor(.blue)
                    }
                }
            }
            .padding(10)
        }
        .background(Color(.systemBackground))
        .cornerRadius(12)
        .shadow(color: .black.opacity(0.1), radius: 8, x: 0, y: 4)
    }
}

// Preview
#Preview {
    ProductCardView(
        product: Product(id: 1, name: "আম", price: 120, imageUrl: "", category: "ফল", rating: 4.5, reviewCount: 100),
        onAddToCart: {},
        onFavorite: {}
    )
    .padding()
}
```

---

## SwiftUI লেআউট

```swift
struct LayoutExamples: View {
    var body: some View {
        ScrollView {
            VStack(spacing: 20) {

                // HStack – আনুভূমিক
                HStack(alignment: .center, spacing: 16) {
                    Image(systemName: "star.fill").foregroundColor(.yellow)
                    Text("রেটিং: ৪.৫")
                    Spacer()
                    Button("কিনুন") { }
                }
                .padding()
                .background(Color(.systemGray6))
                .cornerRadius(10)

                // ZStack – উপরে রাখা
                ZStack(alignment: .topTrailing) {
                    Image("hero-image")
                        .resizable()
                        .aspectRatio(16/9, contentMode: .fill)
                        .frame(height: 200)
                        .clipped()
                        .cornerRadius(12)

                    Text("নতুন")
                        .font(.caption)
                        .fontWeight(.bold)
                        .padding(.horizontal, 8)
                        .padding(.vertical, 4)
                        .background(Color.red)
                        .foregroundColor(.white)
                        .cornerRadius(4)
                        .padding(8)
                }

                // Grid (iOS 16+)
                LazyVGrid(columns: [
                    GridItem(.flexible()),
                    GridItem(.flexible()),
                    GridItem(.flexible())
                ], spacing: 10) {
                    ForEach(0..<9) { index in
                        RoundedRectangle(cornerRadius: 8)
                            .fill(Color.blue.opacity(0.2))
                            .frame(height: 80)
                            .overlay(Text("\(index + 1)"))
                    }
                }

                // ViewThatFits (iOS 16+)
                ViewThatFits {
                    HStack { Text("আনুভূমিক লেআউট"); Button("ঠিক আছে") {} }
                    VStack { Text("উল্লম্ব লেআউট"); Button("ঠিক আছে") {} }
                }

            }
            .padding()
        }
    }
}

// GeometryReader – আকার নির্ধারণ
struct AdaptiveCard: View {
    var body: some View {
        GeometryReader { geometry in
            HStack {
                Image(systemName: "photo")
                    .frame(width: geometry.size.width * 0.3)
                Text("বিষয়বস্তু")
                    .frame(width: geometry.size.width * 0.7)
            }
        }
        .frame(height: 100)
    }
}
```

---

## SwiftUI উইজেট

```swift
struct WidgetShowcase: View {
    @State private var text = ""
    @State private var isOn = false
    @State private var sliderValue: Double = 50
    @State private var selectedOption = "আম"
    @State private var selectedDate = Date()

    var body: some View {
        Form {
            // Text
            Text("সাধারণ টেক্সট")
                .font(.title2)
                .bold()
                .italic()
                .underline()
                .foregroundColor(.primary)

            Label("গুরুত্বপূর্ণ", systemImage: "exclamationmark.triangle")
                .foregroundColor(.orange)

            // TextField
            TextField("নাম লিখুন", text: $text)
                .textFieldStyle(.roundedBorder)
                .autocorrectionDisabled()

            SecureField("পাসওয়ার্ড", text: $text)

            // Toggle
            Toggle("নোটিফিকেশন চালু", isOn: $isOn)
                .tint(.green)

            // Slider
            VStack(alignment: .leading) {
                Text("মূল্য সীমা: ৳\(Int(sliderValue))")
                Slider(value: $sliderValue, in: 0...10000, step: 100)
                    .tint(.blue)
            }

            // Picker
            Picker("পণ্য", selection: $selectedOption) {
                ForEach(["আম", "কলা", "লিচু"], id: \.self) { item in
                    Text(item).tag(item)
                }
            }

            // Date Picker
            DatePicker("তারিখ", selection: $selectedDate, displayedComponents: .date)
                .datePickerStyle(.compact)
                .environment(\.locale, Locale(identifier: "bn_BD"))

            // Stepper
            Stepper("পরিমাণ: \(Int(sliderValue))", value: $sliderValue, in: 1...100)

            // Button varieties
            Group {
                Button("সাধারণ বাটন") { }
                Button("বিপজ্জনক", role: .destructive) { }
                Button("বাতিল", role: .cancel) { }
            }
            .buttonStyle(.bordered)

            // Image
            Image(systemName: "heart.fill")
                .font(.largeTitle)
                .foregroundColor(.red)
                .symbolEffect(.bounce)

            // ProgressView
            ProgressView(value: 0.7) { Text("অগ্রগতি") }
                .tint(.blue)

            ProgressView().progressViewStyle(.circular)
        }
    }
}
```

---

## State ও Binding

```swift
// @State – স্থানীয় পরিবর্তনযোগ্য মান
struct CounterView: View {
    @State private var count = 0
    @State private var isExpanded = false

    var body: some View {
        VStack {
            Text("গণনা: \(count)")
                .font(.largeTitle)
                .contentTransition(.numericText())

            HStack(spacing: 20) {
                Button("-") { count -= 1 }.buttonStyle(.borderedProminent)
                Button("রিসেট") { count = 0 }.buttonStyle(.bordered)
                Button("+") { count += 1 }.buttonStyle(.borderedProminent).tint(.green)
            }
        }
    }
}

// @Binding – প্যারেন্ট থেকে মান
struct ToggleRow: View {
    @Binding var isEnabled: Bool
    let title: String

    var body: some View {
        HStack {
            Text(title)
            Spacer()
            Toggle("", isOn: $isEnabled)
        }
    }
}

// @ObservableObject ও @StateObject (iOS 14)
class ProductViewModel: ObservableObject {
    @Published var products: [Product] = []
    @Published var isLoading = false
    @Published var searchText = ""
    @Published var selectedCategory: String?

    var filteredProducts: [Product] {
        products.filter { product in
            (searchText.isEmpty || product.name.localizedCaseInsensitiveContains(searchText)) &&
            (selectedCategory == nil || product.category == selectedCategory)
        }
    }

    func loadProducts() async {
        await MainActor.run { isLoading = true }
        do {
            let fetched = try await ProductService().getProducts()
            await MainActor.run {
                self.products = fetched
                self.isLoading = false
            }
        } catch {
            await MainActor.run { isLoading = false }
        }
    }
}

// @Observable (iOS 17+ – আধুনিক পদ্ধতি)
@Observable
class CartViewModel {
    var items: [CartItem] = []
    var total: Double { items.reduce(0) { $0 + $1.product.price * Double($1.quantity) } }
    var itemCount: Int { items.reduce(0) { $0 + $1.quantity } }

    func add(_ product: Product) {
        if let index = items.firstIndex(where: { $0.product.id == product.id }) {
            items[index].quantity += 1
        } else {
            items.append(CartItem(product: product, quantity: 1))
        }
    }
}

// @EnvironmentObject – গ্লোবাল স্টেট
struct ContentView: View {
    @StateObject var cartViewModel = CartViewModel()

    var body: some View {
        TabView {
            HomeView().tabItem { Label("হোম", systemImage: "house") }
            CartView().tabItem {
                Label("কার্ট \(cartViewModel.itemCount)", systemImage: "cart")
            }
        }
        .environmentObject(cartViewModel)
    }
}

struct CartView: View {
    @EnvironmentObject var cart: CartViewModel  // inject হয়

    var body: some View {
        Text("মোট: ৳\(cart.total, specifier: "%.2f")")
    }
}

// @AppStorage – UserDefaults-এর সাথে সংযুক্ত
struct SettingsView: View {
    @AppStorage("isDarkMode") private var isDarkMode = false
    @AppStorage("userName") private var userName = ""

    var body: some View {
        Form {
            Toggle("ডার্ক মোড", isOn: $isDarkMode)
            TextField("নাম", text: $userName)
        }
    }
}
```

---

## List ও ForEach

```swift
struct ProductListView: View {
    @StateObject var viewModel = ProductViewModel()

    var body: some View {
        NavigationStack {
            Group {
                if viewModel.isLoading {
                    ProgressView("লোড হচ্ছে...").frame(maxWidth: .infinity, maxHeight: .infinity)
                } else if viewModel.filteredProducts.isEmpty {
                    ContentUnavailableView("পণ্য নেই", systemImage: "cart", description: Text("অনুসন্ধান পরিবর্তন করুন"))
                } else {
                    List {
                        // Section সহ
                        ForEach(groupedProducts.keys.sorted(), id: \.self) { category in
                            Section(category) {
                                ForEach(groupedProducts[category] ?? []) { product in
                                    NavigationLink(value: product) {
                                        ProductRowView(product: product)
                                    }
                                    .swipeActions(edge: .trailing) {
                                        Button(role: .destructive) {
                                            viewModel.delete(product)
                                        } label: {
                                            Label("মুছুন", systemImage: "trash")
                                        }

                                        Button {
                                            viewModel.toggleFavorite(product)
                                        } label: {
                                            Label("পছন্দ", systemImage: "heart")
                                        }.tint(.pink)
                                    }
                                    .contextMenu {
                                        Button("শেয়ার", systemImage: "square.and.arrow.up") { }
                                        Button("কার্টে যোগ", systemImage: "cart.badge.plus") { }
                                        Divider()
                                        Button("মুছুন", systemImage: "trash", role: .destructive) { }
                                    }
                                }
                            }
                        }
                    }
                    .listStyle(.insetGrouped)
                    .refreshable { await viewModel.loadProducts() }
                }
            }
            .searchable(text: $viewModel.searchText, prompt: "পণ্য খুঁজুন")
            .navigationTitle("পণ্যসমূহ")
            .navigationDestination(for: Product.self) { product in
                ProductDetailView(product: product)
            }
            .task { await viewModel.loadProducts() }
            .toolbar {
                ToolbarItem(placement: .topBarTrailing) {
                    Menu {
                        Button("মূল্য: কম থেকে বেশি") { viewModel.sort(by: .priceLow) }
                        Button("মূল্য: বেশি থেকে কম") { viewModel.sort(by: .priceHigh) }
                        Button("নাম (A-Z)") { viewModel.sort(by: .name) }
                    } label: {
                        Image(systemName: "arrow.up.arrow.down")
                    }
                }
            }
        }
    }

    var groupedProducts: [String: [Product]] {
        Dictionary(grouping: viewModel.filteredProducts) { $0.category }
    }
}

// LazyVStack – স্ক্রলের সময় lazy লোড
struct InfiniteScrollView: View {
    @StateObject var viewModel = InfiniteViewModel()

    var body: some View {
        ScrollView {
            LazyVStack(spacing: 8) {
                ForEach(viewModel.items) { item in
                    ItemRow(item: item)
                        .onAppear {
                            if item == viewModel.items.last {
                                Task { await viewModel.loadMore() }
                            }
                        }
                }
                if viewModel.isLoadingMore {
                    ProgressView()
                }
            }
            .padding()
        }
    }
}
```

---

## SwiftUI Navigation

```swift
// NavigationStack (iOS 16+) – সুপারিশকৃত
struct AppNavigationView: View {
    @State private var path = NavigationPath()

    var body: some View {
        NavigationStack(path: $path) {
            HomeView(path: $path)
                .navigationDestination(for: Product.self) { product in
                    ProductDetailView(product: product)
                }
                .navigationDestination(for: String.self) { route in
                    switch route {
                    case "cart": CartView()
                    case "profile": ProfileView()
                    default: EmptyView()
                    }
                }
        }
    }
}

// TabView
struct MainTabView: View {
    @State private var selectedTab = 0
    @StateObject var cartVM = CartViewModel()

    var body: some View {
        TabView(selection: $selectedTab) {
            HomeView()
                .tabItem { Label("হোম", systemImage: "house.fill") }
                .tag(0)

            SearchView()
                .tabItem { Label("খুঁজুন", systemImage: "magnifyingglass") }
                .tag(1)

            CartView()
                .badge(cartVM.itemCount)
                .tabItem { Label("কার্ট", systemImage: "cart.fill") }
                .tag(2)

            ProfileView()
                .tabItem { Label("প্রোফাইল", systemImage: "person.fill") }
                .tag(3)
        }
        .environmentObject(cartVM)
        .tint(.blue)
    }
}

// Sheet ও FullScreenCover
struct SheetExample: View {
    @State private var showSheet = false
    @State private var showFullScreen = false

    var body: some View {
        VStack {
            Button("শিট দেখান") { showSheet = true }
            Button("ফুলস্ক্রিন দেখান") { showFullScreen = true }
        }
        .sheet(isPresented: $showSheet) {
            FilterSheet()
                .presentationDetents([.medium, .large])
                .presentationDragIndicator(.visible)
        }
        .fullScreenCover(isPresented: $showFullScreen) {
            CameraView(isPresented: $showFullScreen)
        }
    }
}

// Alert ও Confirmation Dialog
struct AlertExample: View {
    @State private var showAlert = false
    @State private var showDialog = false

    var body: some View {
        VStack {
            Button("Alert") { showAlert = true }
            Button("Dialog") { showDialog = true }
        }
        .alert("নিশ্চিত করুন", isPresented: $showAlert) {
            Button("মুছুন", role: .destructive) { /* মুছুন */ }
            Button("বাতিল", role: .cancel) { }
        } message: {
            Text("এই পণ্যটি মুছে ফেলা হবে।")
        }
        .confirmationDialog("বিকল্প", isPresented: $showDialog) {
            Button("ক্যামেরা") { }
            Button("গ্যালারি") { }
            Button("বাতিল", role: .cancel) { }
        }
    }
}
```

---

## SwiftUI অ্যানিমেশন

```swift
struct AnimationShowcase: View {
    @State private var isExpanded = false
    @State private var rotation: Double = 0
    @State private var scale: CGFloat = 1.0
    @State private var showCard = false
    @State private var count = 0

    var body: some View {
        ScrollView {
            VStack(spacing: 30) {

                // withAnimation
                Button("প্রসারিত করুন") {
                    withAnimation(.spring(response: 0.5, dampingFraction: 0.7)) {
                        isExpanded.toggle()
                    }
                }
                .buttonStyle(.borderedProminent)

                RoundedRectangle(cornerRadius: 12)
                    .fill(Color.blue)
                    .frame(width: isExpanded ? 300 : 100, height: isExpanded ? 200 : 100)
                    .animation(.easeInOut(duration: 0.4), value: isExpanded)

                // Rotation
                Image(systemName: "gear.circle.fill")
                    .font(.system(size: 60))
                    .foregroundColor(.blue)
                    .rotationEffect(.degrees(rotation))
                    .onTapGesture {
                        withAnimation(.linear(duration: 1)) { rotation += 360 }
                    }

                // Scale
                Circle()
                    .fill(Color.green)
                    .frame(width: 80 * scale, height: 80 * scale)
                    .scaleEffect(scale)
                    .onTapGesture {
                        withAnimation(.spring()) { scale = scale == 1.0 ? 1.5 : 1.0 }
                    }

                // Transition
                if showCard {
                    RoundedRectangle(cornerRadius: 12)
                        .fill(Color.orange)
                        .frame(height: 100)
                        .transition(.asymmetric(insertion: .slide, removal: .opacity))
                }
                Button(showCard ? "লুকান" : "দেখান") {
                    withAnimation { showCard.toggle() }
                }

                // contentTransition
                Text("\(count)")
                    .font(.largeTitle)
                    .bold()
                    .contentTransition(.numericText())
                Button("+") { withAnimation { count += 1 } }

                // Repeating animation
                Image(systemName: "heart.fill")
                    .foregroundColor(.red)
                    .font(.largeTitle)
                    .symbolEffect(.bounce, value: count)
                    .symbolEffect(.pulse)
            }
            .padding()
        }
    }
}
```

---

## SwiftUI Form

```swift
struct RegistrationForm: View {
    @State private var name = ""
    @State private var email = ""
    @State private var phone = ""
    @State private var password = ""
    @State private var selectedGender = "পুরুষ"
    @State private var birthDate = Date()
    @State private var agreeToTerms = false
    @State private var isLoading = false
    @State private var showAlert = false
    @State private var alertMessage = ""

    private var isFormValid: Bool {
        !name.isEmpty && email.isValidEmail && !password.isEmpty && agreeToTerms
    }

    var body: some View {
        NavigationStack {
            Form {
                Section("ব্যক্তিগত তথ্য") {
                    TextField("পুরো নাম *", text: $name)
                    Picker("লিঙ্গ", selection: $selectedGender) {
                        ForEach(["পুরুষ", "মহিলা", "অন্যান্য"], id: \.self) { Text($0) }
                    }
                    DatePicker("জন্ম তারিখ", selection: $birthDate, displayedComponents: .date)
                }

                Section("যোগাযোগ") {
                    TextField("ইমেইল *", text: $email)
                        .keyboardType(.emailAddress)
                        .autocorrectionDisabled()
                        .textInputAutocapitalization(.never)
                        .overlay(
                            Image(systemName: email.isEmpty ? "" : (email.isValidEmail ? "checkmark.circle.fill" : "xmark.circle.fill"))
                                .foregroundColor(email.isValidEmail ? .green : .red)
                                .padding(.trailing, 8),
                            alignment: .trailing
                        )

                    TextField("ফোন", text: $phone)
                        .keyboardType(.phonePad)
                }

                Section("নিরাপত্তা") {
                    SecureField("পাসওয়ার্ড *", text: $password)
                    if !password.isEmpty && password.count < 8 {
                        Label("কমপক্ষে ৮ অক্ষর প্রয়োজন", systemImage: "exclamationmark.circle")
                            .font(.caption)
                            .foregroundColor(.red)
                    }
                }

                Section {
                    Toggle("আমি শর্তাবলীতে সম্মত", isOn: $agreeToTerms)
                }

                Section {
                    Button {
                        submit()
                    } label: {
                        HStack {
                            Spacer()
                            if isLoading {
                                ProgressView()
                            } else {
                                Text("নিবন্ধন করুন")
                                    .fontWeight(.semibold)
                            }
                            Spacer()
                        }
                    }
                    .disabled(!isFormValid || isLoading)
                    .listRowBackground(isFormValid ? Color.blue : Color.gray)
                    .foregroundColor(.white)
                }
            }
            .navigationTitle("নিবন্ধন")
            .alert("বার্তা", isPresented: $showAlert) {
                Button("ঠিক আছে") { }
            } message: {
                Text(alertMessage)
            }
        }
    }

    private func submit() {
        isLoading = true
        Task {
            try? await Task.sleep(nanoseconds: 2_000_000_000)
            await MainActor.run {
                isLoading = false
                alertMessage = "নিবন্ধন সফল হয়েছে!"
                showAlert = true
            }
        }
    }
}
```

---

# চতুর্থ ভাগ – Architecture ও ডেটা

## MVVM আর্কিটেকচার

```
┌──────────────────────────────────────────┐
│              View (SwiftUI/UIKit)         │
│   - শুধু UI দেখায়                        │
│   - User Events পাঠায়                   │
└──────────────┬───────────────────────────┘
               │ observe / action
┌──────────────▼───────────────────────────┐
│               ViewModel                   │
│   - Business Logic                        │
│   - @Published / @Observable              │
└──────────────┬───────────────────────────┘
               │ data access
┌──────────────▼───────────────────────────┐
│              Repository                   │
│   - ডেটা উৎস নির্ধারণ                   │
└───────┬─────────────────────┬────────────┘
        │                     │
┌───────▼──────┐    ┌─────────▼──────────┐
│  Core Data   │    │  URLSession (API)   │
│  (স্থানীয়)  │    │  (রিমোট)           │
└──────────────┘    └────────────────────┘
```

```swift
// Repository Protocol
protocol ProductRepositoryProtocol {
    func getProducts() async throws -> [Product]
    func getProduct(id: Int) async throws -> Product
    func searchProducts(query: String) async throws -> [Product]
}

// Repository Implementation
class ProductRepository: ProductRepositoryProtocol {
    private let apiService: APIServiceProtocol
    private let cacheService: CacheServiceProtocol

    init(apiService: APIServiceProtocol = APIService(), cacheService: CacheServiceProtocol = CacheService()) {
        self.apiService = apiService
        self.cacheService = cacheService
    }

    func getProducts() async throws -> [Product] {
        if let cached = cacheService.getProducts(), !cached.isEmpty {
            return cached
        }
        let products = try await apiService.fetchProducts()
        cacheService.save(products)
        return products
    }

    func getProduct(id: Int) async throws -> Product {
        try await apiService.fetchProduct(id: id)
    }

    func searchProducts(query: String) async throws -> [Product] {
        try await apiService.searchProducts(query: query)
    }
}
```

---

## Combine Framework

```swift
import Combine

class SearchViewModel: ObservableObject {
    @Published var searchQuery = ""
    @Published var results: [Product] = []
    @Published var isLoading = false
    @Published var error: String?

    private var cancellables = Set<AnyCancellable>()
    private let repository: ProductRepositoryProtocol

    init(repository: ProductRepositoryProtocol = ProductRepository()) {
        self.repository = repository
        setupSearchPipeline()
    }

    private func setupSearchPipeline() {
        $searchQuery
            .debounce(for: .milliseconds(500), scheduler: RunLoop.main)  // ৫০০ms অপেক্ষা
            .removeDuplicates()  // একই কোয়েরি দুইবার নয়
            .filter { !$0.isEmpty }  // খালি কোয়েরি নয়
            .flatMap { [weak self] query -> AnyPublisher<[Product], Never> in
                guard let self = self else { return Just([]).eraseToAnyPublisher() }
                return Future { promise in
                    Task {
                        do {
                            let results = try await self.repository.searchProducts(query: query)
                            promise(.success(results))
                        } catch {
                            promise(.success([]))
                        }
                    }
                }
                .eraseToAnyPublisher()
            }
            .receive(on: DispatchQueue.main)
            .assign(to: &$results)
    }
}

// Publisher তৈরি
extension URLSession {
    func dataTaskPublisher<T: Decodable>(for url: URL, type: T.Type) -> AnyPublisher<T, Error> {
        dataTaskPublisher(for: url)
            .map(\.data)
            .decode(type: T.self, decoder: JSONDecoder())
            .eraseToAnyPublisher()
    }
}
```

---

## Core Data

```swift
// Model তৈরি: Xcode → File → New → Data Model

// Core Data Stack
class PersistenceController {
    static let shared = PersistenceController()

    let container: NSPersistentContainer

    init(inMemory: Bool = false) {
        container = NSPersistentContainer(name: "MyApp")
        if inMemory {
            container.persistentStoreDescriptions.first!.url = URL(fileURLWithPath: "/dev/null")
        }
        container.loadPersistentStores { _, error in
            if let error = error { fatalError("Core Data ত্রুটি: \(error)") }
        }
        container.viewContext.automaticallyMergesChangesFromParent = true
    }
}

// CRUD অপারেশন
class ProductDataManager {
    private var context: NSManagedObjectContext

    init(context: NSManagedObjectContext = PersistenceController.shared.container.viewContext) {
        self.context = context
    }

    // তৈরি করা
    func createProduct(name: String, price: Double, category: String) {
        let product = ProductEntity(context: context)
        product.id = UUID()
        product.name = name
        product.price = price
        product.category = category
        product.createdAt = Date()
        save()
    }

    // পড়া
    func fetchProducts(category: String? = nil) -> [ProductEntity] {
        let request: NSFetchRequest<ProductEntity> = ProductEntity.fetchRequest()
        if let category = category {
            request.predicate = NSPredicate(format: "category == %@", category)
        }
        request.sortDescriptors = [NSSortDescriptor(key: "name", ascending: true)]
        return (try? context.fetch(request)) ?? []
    }

    // আপডেট
    func update(product: ProductEntity, newPrice: Double) {
        product.price = newPrice
        save()
    }

    // মুছে ফেলা
    func delete(_ product: ProductEntity) {
        context.delete(product)
        save()
    }

    private func save() {
        guard context.hasChanges else { return }
        try? context.save()
    }
}

// SwiftUI-তে Core Data (@FetchRequest)
struct CoreDataProductList: View {
    @Environment(\.managedObjectContext) private var viewContext

    @FetchRequest(
        sortDescriptors: [NSSortDescriptor(keyPath: \ProductEntity.name, ascending: true)],
        predicate: NSPredicate(format: "price < %f", 500.0),
        animation: .default
    )
    private var products: FetchedResults<ProductEntity>

    var body: some View {
        List(products) { product in
            Text(product.name ?? "")
        }
        .onAppear {
            let manager = ProductDataManager(context: viewContext)
            manager.createProduct(name: "আম", price: 120, category: "ফল")
        }
    }
}
```

---

## URLSession ও Networking

```swift
// API Service
protocol APIServiceProtocol {
    func fetchProducts() async throws -> [Product]
    func fetchProduct(id: Int) async throws -> Product
    func searchProducts(query: String) async throws -> [Product]
    func createProduct(_ product: CreateProductRequest) async throws -> Product
}

struct APIService: APIServiceProtocol {
    private let baseURL = URL(string: "https://api.example.com/v1")!
    private let session: URLSession

    init() {
        let config = URLSessionConfiguration.default
        config.timeoutIntervalForRequest = 30
        config.timeoutIntervalForResource = 60
        session = URLSession(configuration: config)
    }

    func fetchProducts() async throws -> [Product] {
        try await fetch(endpoint: "/products")
    }

    func fetchProduct(id: Int) async throws -> Product {
        try await fetch(endpoint: "/products/\(id)")
    }

    func searchProducts(query: String) async throws -> [Product] {
        var components = URLComponents(url: baseURL.appendingPathComponent("/products"), resolvingAgainstBaseURL: false)!
        components.queryItems = [URLQueryItem(name: "search", value: query)]
        return try await fetch(url: components.url!)
    }

    func createProduct(_ product: CreateProductRequest) async throws -> Product {
        var request = URLRequest(url: baseURL.appendingPathComponent("/products"))
        request.httpMethod = "POST"
        request.setValue("application/json", forHTTPHeaderField: "Content-Type")
        request.httpBody = try JSONEncoder().encode(product)
        return try await fetch(request: request)
    }

    // Generic fetch
    private func fetch<T: Decodable>(endpoint: String) async throws -> T {
        try await fetch(url: baseURL.appendingPathComponent(endpoint))
    }

    private func fetch<T: Decodable>(url: URL) async throws -> T {
        var request = URLRequest(url: url)
        request.setValue("application/json", forHTTPHeaderField: "Accept")
        if let token = TokenManager.shared.token {
            request.setValue("Bearer \(token)", forHTTPHeaderField: "Authorization")
        }
        return try await fetch(request: request)
    }

    private func fetch<T: Decodable>(request: URLRequest) async throws -> T {
        let (data, response) = try await session.data(for: request)

        guard let httpResponse = response as? HTTPURLResponse else {
            throw AppError.invalidData
        }

        switch httpResponse.statusCode {
        case 200...299:
            do {
                let decoder = JSONDecoder()
                decoder.keyDecodingStrategy = .convertFromSnakeCase
                decoder.dateDecodingStrategy = .iso8601
                return try decoder.decode(T.self, from: data)
            } catch {
                throw AppError.decodingError(error)
            }
        case 401: throw AppError.unauthorized
        case 404: throw AppError.notFound(id: 0)
        default: throw AppError.serverError(code: httpResponse.statusCode)
        }
    }
}
```

---

## JSON Codable

```swift
// সহজ Codable
struct Product: Codable, Identifiable {
    let id: Int
    let name: String
    let price: Double
    let imageUrl: String
    let category: String

    enum CodingKeys: String, CodingKey {
        case id, name, price, category
        case imageUrl = "image_url"  // স্নেক কেস → ক্যামেল কেস
    }
}

// Custom Encoding/Decoding
struct CustomProduct: Codable {
    let id: Int
    let name: String
    let price: Price

    struct Price: Codable {
        let amount: Double
        let currency: String
    }
}

// Pagination Response
struct PaginatedResponse<T: Codable>: Codable {
    let data: [T]
    let total: Int
    let page: Int
    let perPage: Int
    let hasMore: Bool

    enum CodingKeys: String, CodingKey {
        case data, total, page
        case perPage = "per_page"
        case hasMore = "has_more"
    }
}

// JSON পার্সিং
func parseProducts(from jsonString: String) throws -> [Product] {
    let decoder = JSONDecoder()
    decoder.keyDecodingStrategy = .convertFromSnakeCase
    decoder.dateDecodingStrategy = .iso8601

    guard let data = jsonString.data(using: .utf8) else {
        throw AppError.invalidData
    }
    return try decoder.decode([Product].self, from: data)
}

// JSON এনকোডিং
func encodeProduct(_ product: Product) throws -> Data {
    let encoder = JSONEncoder()
    encoder.keyEncodingStrategy = .convertToSnakeCase
    encoder.outputFormatting = [.prettyPrinted, .sortedKeys]
    return try encoder.encode(product)
}
```

---

## UserDefaults ও Keychain

```swift
// UserDefaults – সাধারণ ডেটা
@propertyWrapper
struct UserDefault<T> {
    let key: String
    let defaultValue: T
    let storage: UserDefaults

    init(_ key: String, defaultValue: T, storage: UserDefaults = .standard) {
        self.key = key
        self.defaultValue = defaultValue
        self.storage = storage
    }

    var wrappedValue: T {
        get { storage.object(forKey: key) as? T ?? defaultValue }
        set { storage.set(newValue, forKey: key) }
    }
}

// ব্যবহার
class AppSettings {
    @UserDefault("is_dark_mode", defaultValue: false)
    var isDarkMode: Bool

    @UserDefault("language", defaultValue: "bn")
    var language: String

    @UserDefault("notification_enabled", defaultValue: true)
    var notificationEnabled: Bool

    func reset() {
        UserDefaults.standard.removePersistentDomain(forName: Bundle.main.bundleIdentifier!)
    }
}

// Keychain – সংবেদনশীল ডেটা (token, password)
class KeychainManager {
    static let shared = KeychainManager()

    func save(key: String, value: String) {
        guard let data = value.data(using: .utf8) else { return }
        let query: [String: Any] = [
            kSecClass as String: kSecClassGenericPassword,
            kSecAttrAccount as String: key,
            kSecValueData as String: data,
            kSecAttrAccessible as String: kSecAttrAccessibleWhenUnlockedThisDeviceOnly
        ]
        SecItemDelete(query as CFDictionary)
        SecItemAdd(query as CFDictionary, nil)
    }

    func get(key: String) -> String? {
        let query: [String: Any] = [
            kSecClass as String: kSecClassGenericPassword,
            kSecAttrAccount as String: key,
            kSecReturnData as String: true,
            kSecMatchLimit as String: kSecMatchLimitOne
        ]
        var result: AnyObject?
        SecItemCopyMatching(query as CFDictionary, &result)
        guard let data = result as? Data else { return nil }
        return String(data: data, encoding: .utf8)
    }

    func delete(key: String) {
        let query: [String: Any] = [
            kSecClass as String: kSecClassGenericPassword,
            kSecAttrAccount as String: key
        ]
        SecItemDelete(query as CFDictionary)
    }
}
```

---

## Dependency Injection

```swift
// Protocol-based DI
protocol HTTPClientProtocol {
    func get<T: Decodable>(url: URL) async throws -> T
    func post<T: Decodable, B: Encodable>(url: URL, body: B) async throws -> T
}

class DependencyContainer {
    static let shared = DependencyContainer()

    lazy var httpClient: HTTPClientProtocol = URLSessionHTTPClient()
    lazy var productRepository: ProductRepositoryProtocol = ProductRepository(httpClient: httpClient)
    lazy var cartRepository: CartRepositoryProtocol = CartRepository()

    lazy var productViewModel = ProductViewModel(repository: productRepository)
    lazy var cartViewModel = CartViewModel(repository: cartRepository)
}

// SwiftUI-তে
@main
struct MyApp: App {
    private let container = DependencyContainer.shared

    var body: some Scene {
        WindowGroup {
            ContentView()
                .environmentObject(container.productViewModel)
                .environmentObject(container.cartViewModel)
        }
    }
}
```

---

# পঞ্চম ভাগ – উন্নত বিষয়

## Firebase ইন্টিগ্রেশন

```swift
// SPM: https://github.com/firebase/firebase-ios-sdk

// AppDelegate.swift
import FirebaseCore

class AppDelegate: NSObject, UIApplicationDelegate {
    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]? = nil) -> Bool {
        FirebaseApp.configure()
        return true
    }
}

// Authentication
import FirebaseAuth

class AuthService {
    static let shared = AuthService()

    var currentUser: User? { Auth.auth().currentUser }

    func signIn(email: String, password: String) async throws -> User {
        let result = try await Auth.auth().signIn(withEmail: email, password: password)
        return result.user
    }

    func signUp(email: String, password: String, name: String) async throws -> User {
        let result = try await Auth.auth().createUser(withEmail: email, password: password)
        let changeRequest = result.user.createProfileChangeRequest()
        changeRequest.displayName = name
        try await changeRequest.commitChanges()
        return result.user
    }

    func signOut() throws {
        try Auth.auth().signOut()
    }

    func resetPassword(email: String) async throws {
        try await Auth.auth().sendPasswordReset(withEmail: email)
    }

    var authStatePublisher: AnyPublisher<User?, Never> {
        Publishers.Create { subscriber in
            let handle = Auth.auth().addStateDidChangeListener { _, user in
                subscriber.send(user)
            }
            return AnyCancellable { Auth.auth().removeStateDidChangeListener(handle) }
        }
        .eraseToAnyPublisher()
    }
}

// Firestore
import FirebaseFirestore

class ProductFirestoreService {
    private let db = Firestore.firestore()
    private var productsRef: CollectionReference { db.collection("products") }

    // যোগ করা
    func addProduct(_ product: Product) async throws {
        let data: [String: Any] = [
            "name": product.name,
            "price": product.price,
            "category": product.category,
            "imageUrl": product.imageUrl,
            "createdAt": FieldValue.serverTimestamp()
        ]
        try await productsRef.addDocument(data: data)
    }

    // রিয়েলটাইম পড়া
    func listenToProducts(completion: @escaping ([Product]) -> Void) -> ListenerRegistration {
        return productsRef
            .order(by: "createdAt", descending: true)
            .addSnapshotListener { snapshot, _ in
                let products = snapshot?.documents.compactMap { doc -> Product? in
                    let data = doc.data()
                    return Product(
                        id: doc.documentID.hashValue,
                        name: data["name"] as? String ?? "",
                        price: data["price"] as? Double ?? 0,
                        imageUrl: data["imageUrl"] as? String ?? "",
                        category: data["category"] as? String ?? "",
                        rating: 0, reviewCount: 0
                    )
                } ?? []
                completion(products)
            }
    }

    // আপডেট
    func updateProduct(id: String, data: [String: Any]) async throws {
        try await productsRef.document(id).updateData(data)
    }

    // মুছে ফেলা
    func deleteProduct(id: String) async throws {
        try await productsRef.document(id).delete()
    }
}
```

---

## Push Notification

```swift
import UserNotifications
import FirebaseMessaging

// AppDelegate
class AppDelegate: NSObject, UIApplicationDelegate, MessagingDelegate, UNUserNotificationCenterDelegate {

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
        FirebaseApp.configure()
        setupNotifications(application)
        return true
    }

    func setupNotifications(_ application: UIApplication) {
        UNUserNotificationCenter.current().delegate = self
        Messaging.messaging().delegate = self

        let authOptions: UNAuthorizationOptions = [.alert, .badge, .sound]
        UNUserNotificationCenter.current().requestAuthorization(options: authOptions) { granted, _ in
            print("নোটিফিকেশন অনুমতি: \(granted)")
        }
        application.registerForRemoteNotifications()
    }

    // FCM Token
    func messaging(_ messaging: Messaging, didReceiveRegistrationToken fcmToken: String?) {
        guard let token = fcmToken else { return }
        print("FCM Token: \(token)")
        // সার্ভারে পাঠান
        sendTokenToServer(token)
    }

    // ফোরগ্রাউন্ড নোটিফিকেশন
    func userNotificationCenter(_ center: UNUserNotificationCenter, willPresent notification: UNNotification) async -> UNNotificationPresentationOptions {
        return [.banner, .badge, .sound]
    }

    // নোটিফিকেশন ক্লিক
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse) async {
        let userInfo = response.notification.request.content.userInfo
        handleNotification(userInfo: userInfo)
    }

    private func handleNotification(userInfo: [AnyHashable: Any]) {
        guard let type = userInfo["type"] as? String else { return }
        switch type {
        case "order": print("অর্ডার নোটিফিকেশন")
        case "promotion": print("প্রমোশন নোটিফিকেশন")
        default: break
        }
    }
}

// Local Notification
class LocalNotificationManager {

    func scheduleNotification(title: String, body: String, date: Date, identifier: String) async {
        let content = UNMutableNotificationContent()
        content.title = title
        content.body = body
        content.sound = .default
        content.badge = 1

        var components = Calendar.current.dateComponents([.year, .month, .day, .hour, .minute], from: date)
        let trigger = UNCalendarNotificationTrigger(dateMatching: components, repeats: false)
        let request = UNNotificationRequest(identifier: identifier, content: content, trigger: trigger)

        try? await UNUserNotificationCenter.current().add(request)
    }

    func cancelNotification(identifier: String) {
        UNUserNotificationCenter.current().removePendingNotificationRequests(withIdentifiers: [identifier])
    }
}
```

---

## Camera ও Photo Library

```swift
import PhotosUI
import AVFoundation

// SwiftUI-তে PHPicker (iOS 14+)
struct ImagePickerView: View {
    @State private var selectedImage: UIImage?
    @State private var showPhotoPicker = false
    @State private var showCamera = false

    var body: some View {
        VStack {
            if let image = selectedImage {
                Image(uiImage: image)
                    .resizable()
                    .aspectRatio(contentMode: .fit)
                    .frame(height: 200)
                    .cornerRadius(12)
            } else {
                RoundedRectangle(cornerRadius: 12)
                    .fill(Color.gray.opacity(0.2))
                    .frame(height: 200)
                    .overlay(Image(systemName: "photo.badge.plus").font(.largeTitle).foregroundColor(.gray))
            }

            HStack {
                Button("গ্যালারি") { showPhotoPicker = true }
                    .buttonStyle(.bordered)
                Button("ক্যামেরা") { showCamera = true }
                    .buttonStyle(.bordered)
            }
        }
        .photosPicker(isPresented: $showPhotoPicker, selection: .constant(nil), matching: .images)
        .sheet(isPresented: $showCamera) {
            CameraView(capturedImage: $selectedImage)
        }
    }
}

// Camera View (UIViewControllerRepresentable)
struct CameraView: UIViewControllerRepresentable {
    @Binding var capturedImage: UIImage?
    @Environment(\.dismiss) var dismiss

    func makeCoordinator() -> Coordinator {
        Coordinator(parent: self)
    }

    func makeUIViewController(context: Context) -> UIImagePickerController {
        let picker = UIImagePickerController()
        picker.sourceType = .camera
        picker.delegate = context.coordinator
        picker.allowsEditing = true
        return picker
    }

    func updateUIViewController(_ uiViewController: UIImagePickerController, context: Context) {}

    class Coordinator: NSObject, UIImagePickerControllerDelegate, UINavigationControllerDelegate {
        let parent: CameraView

        init(parent: CameraView) { self.parent = parent }

        func imagePickerController(_ picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [UIImagePickerController.InfoKey: Any]) {
            if let image = info[.editedImage] as? UIImage ?? info[.originalImage] as? UIImage {
                parent.capturedImage = image
            }
            parent.dismiss()
        }
    }
}
```

---

## MapKit ও Location

```swift
import MapKit
import CoreLocation

// SwiftUI Map (iOS 17+)
struct MapView: View {
    @State private var cameraPosition: MapCameraPosition = .region(
        MKCoordinateRegion(
            center: CLLocationCoordinate2D(latitude: 23.8103, longitude: 90.4125),
            span: MKCoordinateSpan(latitudeDelta: 0.1, longitudeDelta: 0.1)
        )
    )
    @State private var selectedStore: Store?

    let stores: [Store] = [
        Store(id: 1, name: "বাংলা বাজার ঢাকা", coordinate: CLLocationCoordinate2D(latitude: 23.8103, longitude: 90.4125)),
        Store(id: 2, name: "বাংলা বাজার চট্টগ্রাম", coordinate: CLLocationCoordinate2D(latitude: 22.3569, longitude: 91.7832))
    ]

    var body: some View {
        Map(position: $cameraPosition, selection: $selectedStore) {
            ForEach(stores) { store in
                Annotation(store.name, coordinate: store.coordinate) {
                    Image(systemName: "storefront.fill")
                        .foregroundColor(.blue)
                        .background(Circle().fill(.white).padding(-4))
                }
                .tag(store)
            }
            UserAnnotation()
        }
        .mapControls {
            MapUserLocationButton()
            MapCompass()
            MapScaleView()
        }
        .safeAreaInset(edge: .bottom) {
            if let store = selectedStore {
                StoreDetailCard(store: store)
                    .padding()
                    .background(.regularMaterial)
            }
        }
    }
}

// Location Manager
class LocationManager: NSObject, ObservableObject, CLLocationManagerDelegate {
    private let manager = CLLocationManager()

    @Published var userLocation: CLLocation?
    @Published var authorizationStatus: CLAuthorizationStatus = .notDetermined

    override init() {
        super.init()
        manager.delegate = self
        manager.desiredAccuracy = kCLLocationAccuracyBest
    }

    func requestPermission() {
        manager.requestWhenInUseAuthorization()
    }

    func startUpdating() {
        manager.startUpdatingLocation()
    }

    func stopUpdating() {
        manager.stopUpdatingLocation()
    }

    func locationManagerDidChangeAuthorization(_ manager: CLLocationManager) {
        authorizationStatus = manager.authorizationStatus
        if manager.authorizationStatus == .authorizedWhenInUse {
            manager.startUpdatingLocation()
        }
    }

    func locationManager(_ manager: CLLocationManager, didUpdateLocations locations: [CLLocation]) {
        userLocation = locations.last
    }
}

// Geocoding
func getAddressFromCoordinate(_ coordinate: CLLocationCoordinate2D) async -> String? {
    let geocoder = CLGeocoder()
    let location = CLLocation(latitude: coordinate.latitude, longitude: coordinate.longitude)
    let placemarks = try? await geocoder.reverseGeocodeLocation(location)
    let placemark = placemarks?.first
    return [placemark?.thoroughfare, placemark?.locality, placemark?.country].compactMap { $0 }.joined(separator: ", ")
}
```

---

## In-App Purchase

```swift
import StoreKit

// StoreKit 2 (iOS 15+)
class StoreManager: ObservableObject {
    @Published var products: [Product] = []
    @Published var purchasedProductIDs = Set<String>()

    private let productIDs = ["com.example.premium_monthly", "com.example.premium_yearly"]

    init() {
        Task {
            await loadProducts()
            await updatePurchasedProducts()
            listenForTransactions()
        }
    }

    func loadProducts() async {
        products = (try? await Product.products(for: productIDs)) ?? []
    }

    func purchase(_ product: Product) async throws -> Bool {
        let result = try await product.purchase()
        switch result {
        case .success(let verification):
            let transaction = try checkVerification(verification)
            await transaction.finish()
            await updatePurchasedProducts()
            return true
        case .pending: return false
        case .userCancelled: return false
        @unknown default: return false
        }
    }

    func updatePurchasedProducts() async {
        for await result in Transaction.currentEntitlements {
            if case .verified(let transaction) = result {
                purchasedProductIDs.insert(transaction.productID)
            }
        }
    }

    private func checkVerification<T>(_ result: VerificationResult<T>) throws -> T {
        switch result {
        case .unverified: throw AppError.invalidData
        case .verified(let value): return value
        }
    }

    private func listenForTransactions() {
        Task.detached {
            for await result in Transaction.updates {
                if case .verified(let transaction) = result {
                    await transaction.finish()
                    await self.updatePurchasedProducts()
                }
            }
        }
    }
}
```

---

## Widget Extension

```swift
import WidgetKit
import SwiftUI

// Timeline Entry
struct ProductEntry: TimelineEntry {
    let date: Date
    let product: Product?
}

// Timeline Provider
struct ProductWidgetProvider: TimelineProvider {
    typealias Entry = ProductEntry

    func placeholder(in context: Context) -> ProductEntry {
        ProductEntry(date: Date(), product: Product(id: 1, name: "আম", price: 120, imageUrl: "", category: "ফল", rating: 4.5, reviewCount: 0))
    }

    func getSnapshot(in context: Context, completion: @escaping (ProductEntry) -> Void) {
        let entry = ProductEntry(date: Date(), product: nil)
        completion(entry)
    }

    func getTimeline(in context: Context, completion: @escaping (Timeline<ProductEntry>) -> Void) {
        Task {
            let product = try? await ProductService().getTodaysDeal()
            let entry = ProductEntry(date: Date(), product: product)
            let nextUpdate = Calendar.current.date(byAdding: .hour, value: 1, to: Date())!
            let timeline = Timeline(entries: [entry], policy: .after(nextUpdate))
            completion(timeline)
        }
    }
}

// Widget View
struct ProductWidgetView: View {
    var entry: ProductWidgetProvider.Entry
    @Environment(\.widgetFamily) var family

    var body: some View {
        if let product = entry.product {
            VStack(alignment: .leading) {
                Text("আজকের অফার").font(.caption).foregroundColor(.secondary)
                Text(product.name).font(.headline).bold()
                Text(product.formattedPrice).foregroundColor(.green)
            }
            .padding()
            .containerBackground(.fill.tertiary, for: .widget)
        } else {
            Text("কোনো অফার নেই").containerBackground(.fill.tertiary, for: .widget)
        }
    }
}

// Widget Configuration
@main
struct ProductWidget: Widget {
    let kind = "ProductWidget"

    var body: some WidgetConfiguration {
        StaticConfiguration(kind: kind, provider: ProductWidgetProvider()) { entry in
            ProductWidgetView(entry: entry)
        }
        .configurationDisplayName("বাংলা বাজার অফার")
        .description("আজকের সেরা অফার দেখুন")
        .supportedFamilies([.systemSmall, .systemMedium])
    }
}
```

---

## টেস্টিং

### Unit Test
```swift
import XCTest
@testable import MyApp

class ProductViewModelTests: XCTestCase {

    var viewModel: ProductViewModel!
    var mockRepository: MockProductRepository!

    override func setUp() {
        super.setUp()
        mockRepository = MockProductRepository()
        viewModel = ProductViewModel(repository: mockRepository)
    }

    override func tearDown() {
        viewModel = nil
        mockRepository = nil
        super.tearDown()
    }

    func test_loadProducts_success() async {
        // Given
        let expectedProducts = [
            Product(id: 1, name: "আম", price: 120, imageUrl: "", category: "ফল", rating: 4.5, reviewCount: 100)
        ]
        mockRepository.productsToReturn = expectedProducts

        // When
        await viewModel.loadProducts()

        // Then
        XCTAssertEqual(viewModel.products.count, 1)
        XCTAssertEqual(viewModel.products.first?.name, "আম")
        XCTAssertFalse(viewModel.isLoading)
        XCTAssertNil(viewModel.error)
    }

    func test_loadProducts_networkError() async {
        mockRepository.errorToThrow = AppError.networkUnavailable
        await viewModel.loadProducts()

        XCTAssertTrue(viewModel.products.isEmpty)
        XCTAssertNotNil(viewModel.error)
    }

    func test_filterProducts_byCategory() async {
        mockRepository.productsToReturn = [
            Product(id: 1, name: "আম", price: 120, imageUrl: "", category: "ফল", rating: 4.5, reviewCount: 0),
            Product(id: 2, name: "চাল", price: 60, imageUrl: "", category: "শস্য", rating: 4.0, reviewCount: 0)
        ]
        await viewModel.loadProducts()
        viewModel.selectedCategory = "ফল"

        XCTAssertEqual(viewModel.filteredProducts.count, 1)
        XCTAssertEqual(viewModel.filteredProducts.first?.category, "ফল")
    }
}

// Mock Repository
class MockProductRepository: ProductRepositoryProtocol {
    var productsToReturn: [Product] = []
    var errorToThrow: Error?

    func getProducts() async throws -> [Product] {
        if let error = errorToThrow { throw error }
        return productsToReturn
    }

    func getProduct(id: Int) async throws -> Product {
        if let error = errorToThrow { throw error }
        return productsToReturn.first { $0.id == id } ?? productsToReturn[0]
    }

    func searchProducts(query: String) async throws -> [Product] {
        if let error = errorToThrow { throw error }
        return productsToReturn.filter { $0.name.contains(query) }
    }
}
```

### UI Test
```swift
import XCTest

class ProductListUITests: XCTestCase {

    var app: XCUIApplication!

    override func setUp() {
        super.setUp()
        continueAfterFailure = false
        app = XCUIApplication()
        app.launchArguments = ["--UITesting"]
        app.launch()
    }

    func test_productList_displaysProducts() {
        let productList = app.collectionViews["productList"]
        XCTAssertTrue(productList.exists)
        XCTAssertGreaterThan(productList.cells.count, 0)
    }

    func test_searchProduct_filtersResults() {
        let searchBar = app.searchFields["পণ্য খুঁজুন"]
        searchBar.tap()
        searchBar.typeText("আম")
        XCTAssertTrue(app.staticTexts["আম"].exists)
    }

    func test_addToCart_showsCartCount() {
        app.cells.firstMatch.swipeLeft()
        app.buttons["কার্টে যোগ"].tap()
        XCTAssertTrue(app.tabBars.buttons["কার্ট 1"].exists)
    }
}
```

---

## App Store প্রকাশ

### প্রস্তুতি
```
১. App Icons (1024x1024 PNG, আলাদা আলাদা আকার)
২. Launch Screen
৩. Privacy Policy URL
৪. Screenshots (সব ডিভাইস সাইজের জন্য)
৫. App Description (বাংলা ও ইংরেজিতে)
```

### Archive ও Upload
```bash
# Xcode থেকে
# Product → Archive → Distribute App

# Command Line (fastlane)
fastlane release

# Fastfile
lane :release do
  increment_build_number
  build_app(scheme: "MyApp", configuration: "Release")
  upload_to_app_store(
    skip_metadata: false,
    skip_screenshots: false
  )
end
```

### Info.plist প্রয়োজনীয় কী
```xml
<!-- পারমিশনের কারণ বর্ণনা – অবশ্যই প্রয়োজন -->
<key>NSCameraUsageDescription</key>
<string>পণ্যের ছবি তোলার জন্য ক্যামেরা প্রয়োজন</string>

<key>NSPhotoLibraryUsageDescription</key>
<string>গ্যালারি থেকে ছবি নির্বাচনের জন্য</string>

<key>NSLocationWhenInUseUsageDescription</key>
<string>কাছের দোকান খুঁজতে অবস্থান প্রয়োজন</string>

<key>NSFaceIDUsageDescription</key>
<string>নিরাপদ লগইনের জন্য Face ID ব্যবহার</string>
```

---

## সম্পূর্ণ প্রজেক্ট উদাহরণ

### ই-কমার্স অ্যাপ – MVVM + SwiftUI

```swift
// Models/Product.swift
struct Product: Identifiable, Codable, Hashable {
    let id: Int
    let name: String
    let price: Double
    let imageUrl: String
    let category: String
    let rating: Float
    let reviewCount: Int
    var isFavorite: Bool = false

    var formattedPrice: String { "৳\(Int(price))" }

    enum CodingKeys: String, CodingKey {
        case id, name, price, category, rating
        case imageUrl = "image_url"
        case reviewCount = "review_count"
    }
}

// ViewModels/HomeViewModel.swift
@Observable
class HomeViewModel {
    var products: [Product] = []
    var filteredProducts: [Product] = []
    var isLoading = false
    var errorMessage: String?
    var searchText = "" {
        didSet { filterProducts() }
    }
    var selectedCategory: String? {
        didSet { filterProducts() }
    }
    var categories: [String] = []

    private let repository: ProductRepositoryProtocol

    init(repository: ProductRepositoryProtocol = ProductRepository()) {
        self.repository = repository
    }

    func loadProducts() async {
        isLoading = true
        errorMessage = nil
        defer { isLoading = false }

        do {
            products = try await repository.getProducts()
            categories = Array(Set(products.map { $0.category })).sorted()
            filteredProducts = products
        } catch {
            errorMessage = error.localizedDescription
        }
    }

    func toggleFavorite(_ product: Product) {
        if let index = products.firstIndex(where: { $0.id == product.id }) {
            products[index].isFavorite.toggle()
            filterProducts()
        }
    }

    private func filterProducts() {
        filteredProducts = products.filter { product in
            let matchesSearch = searchText.isEmpty ||
                product.name.localizedCaseInsensitiveContains(searchText)
            let matchesCategory = selectedCategory == nil ||
                product.category == selectedCategory
            return matchesSearch && matchesCategory
        }
    }
}

// Views/HomeView.swift
struct HomeView: View {
    @State private var viewModel = HomeViewModel()
    @Environment(CartViewModel.self) var cartVM

    var body: some View {
        NavigationStack {
            ScrollView {
                LazyVStack(spacing: 0, pinnedViews: .sectionHeaders) {
                    Section {
                        // প্রোমো ব্যানার
                        PromoBannerView()
                            .padding(.horizontal)
                            .padding(.top)

                        // পণ্য গ্রিড
                        LazyVGrid(
                            columns: [GridItem(.flexible()), GridItem(.flexible())],
                            spacing: 12
                        ) {
                            ForEach(viewModel.filteredProducts) { product in
                                NavigationLink(value: product) {
                                    ProductCard(
                                        product: product,
                                        onFavorite: { viewModel.toggleFavorite(product) },
                                        onAddToCart: { cartVM.add(product) }
                                    )
                                }
                                .buttonStyle(.plain)
                            }
                        }
                        .padding(.horizontal)
                        .padding(.bottom)

                    } header: {
                        // ক্যাটাগরি ফিল্টার
                        CategoryFilterView(
                            categories: viewModel.categories,
                            selected: $viewModel.selectedCategory
                        )
                        .background(.regularMaterial)
                    }
                }
            }
            .navigationTitle("বাংলা বাজার 🛒")
            .searchable(text: $viewModel.searchText, prompt: "পণ্য খুঁজুন...")
            .toolbar {
                ToolbarItem(placement: .topBarTrailing) {
                    NavigationLink(value: "cart") {
                        Label("কার্ট", systemImage: "cart.fill")
                            .overlay(alignment: .topTrailing) {
                                if cartVM.itemCount > 0 {
                                    Text("\(cartVM.itemCount)")
                                        .font(.system(size: 10, weight: .bold))
                                        .foregroundColor(.white)
                                        .padding(4)
                                        .background(Color.red)
                                        .clipShape(Circle())
                                        .offset(x: 8, y: -8)
                                }
                            }
                    }
                }
            }
            .navigationDestination(for: Product.self) { product in
                ProductDetailView(product: product)
            }
            .navigationDestination(for: String.self) { route in
                if route == "cart" { CartView() }
            }
            .overlay {
                if viewModel.isLoading {
                    ProgressView("লোড হচ্ছে...")
                        .padding()
                        .background(.regularMaterial, in: RoundedRectangle(cornerRadius: 12))
                }
            }
            .alert("ত্রুটি", isPresented: .constant(viewModel.errorMessage != nil)) {
                Button("পুনরায় চেষ্টা") { Task { await viewModel.loadProducts() } }
            } message: {
                Text(viewModel.errorMessage ?? "")
            }
        }
        .task { await viewModel.loadProducts() }
    }
}

// Views/CategoryFilterView.swift
struct CategoryFilterView: View {
    let categories: [String]
    @Binding var selected: String?

    var body: some View {
        ScrollView(.horizontal, showsIndicators: false) {
            HStack(spacing: 8) {
                CategoryChip(title: "সব", isSelected: selected == nil) {
                    selected = nil
                }
                ForEach(categories, id: \.self) { category in
                    CategoryChip(title: category, isSelected: selected == category) {
                        selected = selected == category ? nil : category
                    }
                }
            }
            .padding(.horizontal)
            .padding(.vertical, 8)
        }
    }
}

struct CategoryChip: View {
    let title: String
    let isSelected: Bool
    let action: () -> Void

    var body: some View {
        Button(action: action) {
            Text(title)
                .font(.subheadline)
                .fontWeight(isSelected ? .semibold : .regular)
                .padding(.horizontal, 16)
                .padding(.vertical, 8)
                .background(isSelected ? Color.blue : Color(.systemGray6))
                .foregroundColor(isSelected ? .white : .primary)
                .clipShape(Capsule())
        }
    }
}

// App Entry Point
@main
struct BanglaShopApp: App {
    @State private var cartVM = CartViewModel()

    var body: some Scene {
        WindowGroup {
            MainTabView()
                .environment(cartVM)
        }
    }
}

struct MainTabView: View {
    @Environment(CartViewModel.self) var cartVM

    var body: some View {
        TabView {
            HomeView()
                .tabItem { Label("হোম", systemImage: "house.fill") }
            SearchView()
                .tabItem { Label("খুঁজুন", systemImage: "magnifyingglass") }
            CartView()
                .badge(cartVM.itemCount)
                .tabItem { Label("কার্ট", systemImage: "cart.fill") }
            ProfileView()
                .tabItem { Label("প্রোফাইল", systemImage: "person.fill") }
        }
        .tint(.blue)
    }
}
```

---

## দরকারী লাইব্রেরি সমূহ

### নেটওয়ার্কিং
- `Alamofire` – সহজ HTTP ক্লায়েন্ট
- `Moya` – টাইপ-নিরাপদ HTTP ক্লায়েন্ট

### ইমেজ
- `SDWebImage` – পরিপক্ক, দ্রুত
- `Kingfisher` – Swift-first ইমেজ লাইব্রেরি
- `Nuke` – আধুনিক, দ্রুত

### ডেটাবেজ
- `CoreData` – Apple-এর অফিসিয়াল (বিল্ট-ইন)
- `GRDB` – SQLite wrapper
- `Realm` – মোবাইল ডেটাবেজ

### UI
- `Lottie` – JSON অ্যানিমেশন
- `SwiftUIX` – SwiftUI এক্সটেনশন
- `Charts` – ডেটা ভিজুয়ালাইজেশন (iOS 16+, বিল্ট-ইন)

### ইউটিলিটি
- `KeychainSwift` – Keychain অ্যাক্সেস
- `SwiftyJSON` – JSON পার্সিং
- `CryptoKit` – ক্রিপ্টোগ্রাফি (বিল্ট-ইন)
- `Combine` – Reactive Programming (বিল্ট-ইন)

---

## Xcode শর্টকাট

| শর্টকাট | কাজ |
|--------|-----|
| ⌘+R | রান করুন |
| ⌘+B | বিল্ড করুন |
| ⌘+. | বন্ধ করুন |
| ⌘+/ | মন্তব্য যোগ/বাদ |
| ⌘+Shift+O | ফাইল খুঁজুন |
| ⌘+Ctrl+E | সব একই নাম পরিবর্তন |
| ⌘+Shift+K | বিল্ড ফোল্ডার মুছুন |
| ⌃+I | কোড ফর্ম্যাট করুন |
| ⌘+Shift+Y | Debug Area দেখান |
| ⌥+Click | সংজ্ঞা দেখুন |

---

## পরবর্তী ধাপ

এই গাইড সম্পন্ন করার পর আপনি প্রস্তুত থাকবেন:

১. **বাস্তব iOS অ্যাপ** তৈরি করতে – ই-কমার্স, সোশ্যাল মিডিয়া, হেলথকেয়ার
২. **Swift Concurrency** গভীরভাবে শিখতে – Actor, Sendable, TaskGroup
৩. **Kotlin Multiplatform (KMP)** ও **React Native** বোঝতে তুলনামূলক জ্ঞান অর্জন করতে
৪. **App Store Connect** ও **TestFlight** ব্যবহার করতে
৫. **visionOS** ও **watchOS** ডেভেলপমেন্ট শুরু করতে
৬. **fastlane** দিয়ে CI/CD পাইপলাইন তৈরি করতে

---

## রিসোর্সসমূহ

- **Apple Developer ডকুমেন্টেশন:** https://developer.apple.com/documentation
- **Swift ডকুমেন্টেশন:** https://www.swift.org/documentation
- **SwiftUI Tutorials:** https://developer.apple.com/tutorials/swiftui
- **Hacking with Swift:** https://www.hackingwithswift.com
- **Ray Wenderlich:** https://www.kodeco.com
- **WWDC Sessions:** https://developer.apple.com/videos
- **Swift Package Index:** https://swiftpackageindex.com
- **iOS Dev Weekly:** https://iosdevweekly.com

---

> **মনে রাখুন:** iOS ডেভেলপমেন্ট শেখার সেরা উপায় হলো বাস্তব অ্যাপ তৈরি করা। UIKit দিয়ে মূল বিষয়গুলো বুঝুন, তারপর SwiftUI শিখুন। Apple-এর অফিসিয়াল Tutorial ও WWDC সেশন দেখুন – এগুলো বিনামূল্যে পাওয়া যায়। Swift Playgrounds দিয়ে ছোট ছোট পরীক্ষা করুন। "Hacking with Swift" এর পল হাডসন আপনার সেরা বন্ধু!
