<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>SESI 9: Extension Methods - Dart | Full Slide 1-14</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica Neue', sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            line-height: 1.5;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: #1e293b;
            border-radius: 1rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: #0f172a;
            color: #f1f5f9;
            padding: 1.5rem 2rem;
            border-bottom: 1px solid #334155;
        }

        .header h1 {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: #facc15;
        }

        .identity {
            background: #334155;
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            display: inline-block;
            font-size: 0.75rem;
            color: #cbd5e1;
        }

        .content {
            padding: 1.5rem;
        }

        .slide-card {
            margin-bottom: 2rem;
            border: 1px solid #334155;
            border-radius: 0.75rem;
            overflow: hidden;
            background: #0f172a;
        }

        .slide-header {
            background: #1e293b;
            padding: 0.75rem 1.25rem;
            border-bottom: 1px solid #334155;
            display: flex;
            align-items: center;
            gap: 0.75rem;
            flex-wrap: wrap;
        }

        .slide-num {
            background: #facc15;
            color: #0f172a;
            padding: 0.2rem 0.7rem;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 700;
        }

        .slide-judul {
            font-size: 1.1rem;
            font-weight: 600;
            color: #facc15;
        }

        .teori-box {
            background: #1e293b;
            padding: 0.75rem 1.25rem;
            margin: 1rem 1.25rem;
            border-radius: 0.5rem;
            border-left: 3px solid #facc15;
            color: #cbd5e1;
            font-size: 0.9rem;
        }

        .teori-box strong {
            color: #facc15;
        }

        .code-wrapped {
            margin: 1rem 1.25rem;
            background: #0a0c15;
            border-radius: 0.5rem;
            overflow-x: auto;
            padding: 0.75rem;
            font-family: 'SF Mono', 'Fira Code', 'Courier New', monospace;
            font-size: 0.7rem;
            color: #a5f3c3;
            white-space: pre-wrap;
            word-break: break-word;
            border: 1px solid #334155;
        }

        .code-wrapped code {
            color: #86efac;
            font-family: inherit;
        }

        .dartpad-container {
            margin: 0.75rem 1.25rem 1.25rem 1.25rem;
            border: 1px solid #334155;
            border-radius: 0.5rem;
            overflow: hidden;
            background: #0a0c15;
        }

        .dartpad-frame {
            width: 100%;
            height: 460px;
            border: none;
            display: block;
        }

        @media (max-width: 640px) {
            .dartpad-frame {
                height: 400px;
            }
            .content {
                padding: 1rem;
            }
            .slide-judul {
                font-size: 1rem;
            }
            .teori-box, .code-wrapped, .dartpad-container {
                margin-left: 1rem;
                margin-right: 1rem;
            }
        }

        .footer-note {
            background: #1e293b;
            text-align: center;
            padding: 0.75rem;
            border-radius: 0.5rem;
            color: #94a3b8;
            margin-top: 1rem;
            font-size: 0.8rem;
            border: 1px solid #334155;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="header">
        <h1>SESI 9: Extension Methods</h1>
        <div class="identity">Rifqi Prayoga | 251410005 | SI2A</div>
        <div style="font-size: 0.7rem; margin-top: 0.5rem; opacity: 0.8;">Durasi: 200 menit | Total Slide: 14</div>
    </div>
    <div class="content">

        <!-- SLIDE 1: Review Sesi 8 – Builder Pattern (halaman 2) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 1</span>
                <span class="slide-judul">Review Sesi 8 – Builder Pattern</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Builder Pattern untuk objek kompleks. Method chaining untuk fluent API. Contoh: Pizza.builder().size('large').addTopping('cheese').build()
            </div>
            <div class="code-wrapped"><code>class ConfigBuilder {    ConfigBuilder host(String h) { return this; }    ConfigBuilder port(int p) { return this; }    Config build() { return Config(); } }</code></div>
        </div>

        <!-- SLIDE 2: Pengantar Extension Methods (halaman 3) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 2</span>
                <span class="slide-judul">Pengantar Extension Methods</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Apa itu? Fitur untuk menambahkan metode baru ke tipe yang sudah ada. Tanpa modifikasi kode asli. Tersedia sejak Dart 2.7. Analog: Memberikan kemampuan baru tanpa mengubah benda aslinya.
            </div>
        </div>

        <!-- SLIDE 3: Masalah Tanpa Extension Methods (halaman 4) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 3</span>
                <span class="slide-judul">Masalah Tanpa Extension Methods</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Utility class yang kurang natural.
            </div>
            <div class="code-wrapped"><code>// Utility class yang kurang natural 
class Stringutils { 
    static String capitalize(String text) { 
        if (text.isEmpty) return text; 
        return text[0].toUpperCase() + text.substring(1); 
    } 
    static bool isEmpty(String text) { 
        return text.contains('@'); 
    } 
    void main(){ 
        // Penggunaan kurang natural 
        var name = 'john'; 
        var capitalized = StringUtils.capitalize(name); // 'John' 
        var isEmpty = StringUtils.isEmpty('test@mail.com'); 
        // Cetak variabel name, capitalized, dan isEmpty 
        print('Original name: $name'); 
        print('Capitalized name: $capitalized'); 
        print('Is "test@mail.com" an email? $isEmpty'); 
    } 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=08cda668c72edf3371197e8a4f90d293&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 3"></iframe>
            </div>
        </div>

        <!-- SLIDE 4: Solusi dengan Extension Methods (halaman 5) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 4</span>
                <span class="slide-judul">Solusi dengan Extension Methods</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension method untuk String.
            </div>
            <div class="code-wrapped"><code>// Extension method untuk String  
extension StringExtensions on String {  
    String capitalize() {  
        if (isEmpty) return this;  
        return this[0].toUpperCase() + substring(1);  
    }  
    bool get isEmail => contains('@');  
    String reverse() {  
        return split('').reversed.join();  
    }  
    void main(){  
        // Penggunaan lebih natural  
        var name = 'john';  
        var capitalized = name.capitalize(); // 'John'  
        var isEmail = 'test@mail.com'.isEmail; // true  
        var reversed = 'hello'.reverse(); // 'olleh'  
        // Cetak variabel  
        print('Original name: $name');  
        print('Capitalized name: $capitalized');  
        print('Is "test@mail.com" an email? $isEmail');  
        print('Reversed "hello": $reversed');  
    }  
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=0944b5196a022b11ae98a5a3dbad28a1&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 4"></iframe>
            </div>
        </div>

        <!-- SLIDE 5: Target Extension (halaman 7) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 5</span>
                <span class="slide-judul">Target Extension</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> 1. Built-in types: String, int, double, List, Map, etc. 2. Custom classes: Kelas buatan sendiri. 3. Generic types: List&lt;T&gt;, Map&lt;K, V&gt;. 4. Nullable types: String?, int?
            </div>
            <div class="code-wrapped"><code>// Extension untuk List<int> 
extension IntListExtensions on List<int> { 
    int get sum => fold(0, (total, item) => total + item); 
    double get average => isEmpty ? 0 : sum / length; 
} 
void main(){ 
    var numbers = [1, 2, 3, 4, 5]; 
    print(numbers.sum); // 15 
    print(numbers.average); // 3.0 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=6d4c32db5a6e6ecae456fdadc64f8117&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 5"></iframe>
            </div>
        </div>

        <!-- SLIDE 6: Generic Extensions (halaman 10) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 6</span>
                <span class="slide-judul">Generic Extensions</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension untuk List&lt;T&gt; generic.
            </div>
            <div class="code-wrapped"><code>// Extension untuk List<T> generic 
extension ListExtensions<T> on List<T> { 
    // Safe get dengan default 
    T? getOrNull(int index) { 
        if (index < 0 || index >= length) return null; 
        return this[index]; 
    } 
    // Split list menjadi chunks 
    List<List<T>> chunk(int size) { 
        var chunks = <List<T>>[]; 
        for (var i = 0; i < length; i += size) { 
            chunks.add(sublist(i, i + size > length ? length : i + size)); 
        } 
        return chunks; 
    } 
    // Distinct items 
    List<T> distinct() { 
        var result = <T>[]; 
        for (var item in this) { 
            if (!result.contains(item)) { 
                result.add(item); 
            } 
        } 
        return result; 
    } 
} 
void main(){ 
    // Penggunaan 
    var numbers = [1, 2, 3, 4, 5, 6, 7]; 
    print(numbers.chunk(3)); // [[1, 2, 3], [4, 5, 6], [7]] 
    print([1, 2, 2, 3, 3, 3].distinct()); // [1, 2, 3] 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=f0f27a10715502eb5f3f4c8f257efe6d&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 6"></iframe>
            </div>
        </div>

        <!-- SLIDE 7: Extension untuk Null Safety (halaman 8) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 7</span>
                <span class="slide-judul">Extension untuk Null Safety</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Safe access untuk nullable string.
            </div>
            <div class="code-wrapped"><code>extension NullableStringExtensions on String? { 
    // Safe access untuk nullable string 
    String orEmpty() => this ?? ''; 
    bool get isNullorEmpty => this == null || this!.isEmpty; 
    bool get isNotNullorEmpty => !isNullorEmpty; 
    String withDefault(String defaultValue) => this ?? defaultValue; 
} 
void main(){ 
    // Penggunaan 
    String? name; 
    print(name.isNullorEmpty); // true 
    print(name.withDefault('Guest')); // 'Guest' 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=bd578cde6f0c4ee18bce5234257cd650&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 7"></iframe>
            </div>
        </div>

        <!-- SLIDE 8: Praktik 1 - Utilities untuk Dart Types (halaman 9) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 8</span>
                <span class="slide-judul">Praktik 1 - Utilities untuk Dart Types</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension NumberExtensions dengan method toRupiah, isBetween, power.
            </div>
            <div class="code-wrapped"><code>extension NumberExtensions on num { 
    // Format ke Rupiah 
    String toRupiah() { 
        return 'Rp${toStringAsFixed(0).replaceAllMapped(RegExp(r'(\d{1,3})(?=(\d{3})+(?!\d))'), (match) => '${match[1]}.')}'; 
    } 
    // Check jika dalam range 
    bool isBetween(num min, num max) { 
        return this >= min && this <= max; 
    } 
    // Pangkat 
    num power(int exponent) { 
        var result = this; 
        for (var i = 1; i < exponent; i++) { 
            result *= this; 
        } 
        return result; 
    } 
} 
void main(){ 
    // Penggunaan 
    var price = 1500000; 
    print(price.toRupiah()); // 'Rp1.500.000' 
    print(5.isBetween(1, 10)); // true 
    print(2.power(3)); // 8 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=cd9744d3778bb68f3a20398121c4a532&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 8"></iframe>
            </div>
        </div>

        <!-- SLIDE 9: Extension tanpa nama (halaman 11) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 9</span>
                <span class="slide-judul">Extension tanpa nama (hanya untuk library yang sama)</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension tanpa nama hanya bisa diakses di file/library yang sama.
            </div>
            <div class="code-wrapped"><code>// File: date_utils.dart  
extension on DateTime {  
    String get toYYYYMMDD {  
        return '${year}-${month.toString().padLeft(2, '0')}-${day.toString().padLeft(2, '0')}';  
    }  
    DateTime get startOfDay {  
        return DateTime(year, month, day);  
    }  
}  
void main() {  
    // Hanya bisa diakses di file ini  
    var today = DateTime.now();  
    print(today.toYYYYMMDD); // '2024-01-22'  
    print(today.startOfDay); // 2026-02-20 00:00:00.000  
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=1a8d8534fb930480ab2ca733b650a6c7&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 9"></iframe>
            </div>
        </div>

        <!-- SLIDE 10: Penanganan Konflik Extension (halaman 12) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 10</span>
                <span class="slide-judul">Penanganan Konflik Extension</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Jika dua extension memiliki method sama, gunakan import dengan prefix atau show/hide.
            </div>
            <div class="code-wrapped"><code>// File: string_extensions.dart 
extension StringCaseExtensions on String { 
    String capitalize() => /* ... */; 
} 
// File: text_utils.dart 
extension TextUtilsExtensions on String { 
    String capitalize() => /* ... berbeda ... */; 
} 
// Solusi: Import dengan prefix atau show/hide 
import 'string_extensions.dart' as se; 
import 'text_utils.dart' hide capitalize; 
void main(){ 
    // Atau pilih salah satu 
    var text = 'hello'; 
    // text.capitalize(); // ERROR: ambiguous 
    se.capitalize(text); // Gunakan dengan prefix 
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=9b68e0520ad9e4e43a819539b6dfb8e7&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 10"></iframe>
            </div>
        </div>

        <!-- SLIDE 11: Extension untuk Custom Classes - Product (halaman 13) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 11</span>
                <span class="slide-judul">Extension untuk Custom Classes - Product</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension untuk Product class.
            </div>
            <div class="code-wrapped"><code>class Product {
    final String name;
    final double price;
    
    Product(this.name, this.price);
}
// Extension untuk formatting double ke Rupiah
extension DoubleRupiahFormatter on double {
    String toRupiah() {
        final intValue = toInt();
        String numberString = intValue.toString();
        String formattedString = '';
        int counter = 0;
        for (int i = numberString.length - 1; i >= 0; i--) {
            formattedString = numberString[i] + formattedString;
            counter++;
            if (counter % 3 == 0 && i != 0) {
                formattedString = '.' + formattedString;
            }
        }
        return 'Rp$formattedString';
    }
}
// Extension untuk Product
extension ProductExtensions on Product {
    Product withDiscount(double percentage) {
        var discountedPrice = price * (1 - percentage / 100);
        return Product(name, discountedPrice);
    }
    String get displayInfo => '$name - ${price.toRupiah()}';
    bool get isExpensive => price > 1000000;
}
void main(){
    var laptop = Product('Laptop', 15000000);
    var discounted = laptop.withDiscount(10);
    print(discounted.displayInfo); 
    print(laptop.isExpensive); 
    var keyboard = Product('Keyboard', 750000);
    print(keyboard.displayInfo);
    print(keyboard.isExpensive);
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=038f09c854de69d94396d8ede8dca225&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 11"></iframe>
            </div>
        </div>

        <!-- SLIDE 12: Extension untuk Custom Classes - DoubleRupiahFormatter & ProductExtensions lanjutan -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 12</span>
                <span class="slide-judul">Extension untuk Custom Classes - DoubleRupiahFormatter &amp; ProductExtensions</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension DoubleRupiahFormatter dan ProductExtensions untuk memformat mata uang dan menghitung diskon.
            </div>
            <div class="code-wrapped"><code>// Extension untuk formatting double ke Rupiah (lanjutan)
extension DoubleRupiahFormatter on double {
    String toRupiah() {
        final intValue = toInt();
        String numberString = intValue.toString();
        String formattedString = '';
        int counter = 0;
        for (int i = numberString.length - 1; i >= 0; i--) {
            formattedString = numberString[i] + formattedString;
            counter++;
            if (counter % 3 == 0 && i != 0) {
                formattedString = '.' + formattedString;
            }
        }
        return 'Rp$formattedString';
    }
}
// Extension untuk Product (lanjutan)
extension ProductExtensions on Product {
    Product withDiscount(double percentage) {
        var discountedPrice = price * (1 - percentage / 100);
        return Product(name, discountedPrice);
    }
    String get displayInfo => '$name - ${price.toRupiah()}';
    bool get isExpensive => price > 1000000;
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=c7efd9765c6882fce9652a850ccdc944&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 12"></iframe>
            </div>
        </div>

        <!-- SLIDE 13: Validator Extension (halaman 15) -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 13</span>
                <span class="slide-judul">Validator Extension</span>
            </div>
            <div class="teori-box">
                <strong>Teori:</strong> Extension untuk validasi data seperti email, nomor telepon, dan lain-lain.
            </div>
            <div class="code-wrapped"><code>extension ValidatorExtension on String {
    bool get isValidEmail => contains('@') && contains('.');
    bool get isValidPhoneNumber {
        final regex = RegExp(r'^[0-9]{10,13}$');
        return regex.hasMatch(this);
    }
    bool get isNullOrEmpty => isEmpty;
    bool hasMinLength(int length) => this.length >= length;
    bool get isAlphabetOnly => RegExp(r'^[a-zA-Z]+$').hasMatch(this);
}
void main(){
    var email = 'user@example.com';
    var phone = '08123456789';
    var name = 'JohnDoe';
    print('Email valid: ${email.isValidEmail}');
    print('Phone valid: ${phone.isValidPhoneNumber}');
    print('Name hanya huruf: ${name.isAlphabetOnly}');
    print('Name minimal 5 karakter: ${name.hasMinLength(5)}');
}</code></div>
            <div class="dartpad-container">
                <iframe class="dartpad-frame" src="https://dartpad.dev/embed-flutter.html?id=cbdce1e49679f0d2bf3cec2c9c8b28ef&theme=dark&run=true" loading="lazy" frameborder="0" allow="scripts; allow-same-origin; allow-forms; allow-popups" allowfullscreen title="DartPad Slide 13"></iframe>
            </div>
        </div>

        <!-- SLIDE 14: Penutup -->
        <div class="slide-card">
            <div class="slide-header">
                <span class="slide-num">SLIDE 14</span>
                <span class="slide-judul">Penutup</span>
            </div>
            <div class="teori-box">
                <strong>Kesimpulan:</strong> Extension methods adalah fitur powerful di Dart yang membuat kode lebih bersih, ekspresif, dan mudah dipelihara. Gunakan dengan bijak sesuai best practices.
            </div>
            <div class="footer-note">
                <strong>SESI 9: Extension Methods</strong> — Rifqi Prayoga | 251410005 | SI2A
            </div>
        </div>

    </div>
</div>
</body>
</html>
