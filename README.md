# 📝 String Analyzer in C

**Name:** Yash Manjre  
**Course:** C Essentials - Cisco Networking Academy  

---

## 📖 Project Description

This project is a simple yet effective implementation of a **String Analyzer in C**, developed as part of the Cisco Networking Academy C Essentials course. The program takes a string input from the user and analyzes it to provide meaningful information such as the number of characters, words, vowels, and consonants.

It demonstrates the practical application of fundamental programming concepts including string handling, loops, and conditional statements.

---

## 🎯 Objective

The objective of this project is to:

- Count the total number of characters  
- Count the number of words  
- Identify and count vowels  
- Identify and count consonants  

---

## 🧠 Concepts Used

- Strings (`char[]`)  
- Loops (`for`, `while`)  
- Conditional statements (`if-else`)  
- Standard functions (`fgets()`, `tolower()`)  

---

## ⚙️ Working of the Program

1. The program takes a string input using `fgets()`.  
2. It initializes counters for characters, words, vowels, and consonants.  
3. A loop iterates through each character of the string.  
4. Each character is analyzed:
   - Vowels (a, e, i, o, u) are counted  
   - Alphabets other than vowels are counted as consonants  
   - Spaces are used to determine word count  
5. The process continues until the end of the string.  
6. The final results are displayed to the user.  

---

## 🧪 Example

**Input:**
Hello World

**Output:**
Characters: 11  
Words: 2  
Vowels: 3  
Consonants: 7  

---

## 💻 C Program

```c
#include <stdio.h>
#include <ctype.h>

int main() {
    char str[200];
    int i = 0, vowels = 0, consonants = 0, words = 1, characters = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    while (str[i] != '\0') {
        char ch = tolower(str[i]);

        if (ch != '\n') {
            characters++;
        }

        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
            vowels++;
        }
        else if (ch >= 'a' && ch <= 'z') {
            consonants++;
        }

        if (ch == ' ' && str[i+1] != ' ' && str[i+1] != '\n') {
            words++;
        }

        i++;
    }

    printf("\n--- String Analysis ---\n");
    printf("Characters: %d\n", characters);
    printf("Words: %d\n", words);
    printf("Vowels: %d\n", vowels);
    printf("Consonants: %d\n", consonants);

    return 0;
}

```

---

## 💡 Applications

- Text processing systems  
- Spell-checking tools  
- Data validation systems  
- Basic natural language processing tasks  

---

## 🚀 Possible Enhancements

- Palindrome checking  
- String reversal  
- Character frequency analysis  
- Case conversion (uppercase/lowercase)  

---

## 🎥 Project Presentation Video

Watch the presentation video here:  
👉 https://drive.google.com/file/d/1u5GyMpUJyIx1OiXowIWZslNzYLbY3Pdc/view?usp=sharing

---

## 🏁 Conclusion

The String Analyzer in C is a simple yet powerful project that demonstrates the practical use of fundamental programming concepts. It highlights how strings, loops, and conditional statements can be combined to analyze text data effectively.

This project strengthens programming fundamentals and prepares learners for more advanced applications in software development.

---

## 👨‍💻 Author

**Yash Manjre**
