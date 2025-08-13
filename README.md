# Sentence Analysis Algorithm (Algo GMC)

## 📌 Overview
This project implements a pseudo-code algorithm using the **Algo GMC** VS Code extension.  
The algorithm reads a sentence **character by character**, assuming:  
- The sentence ends with a period (`.`).  
- The first character is an uppercase letter.  
- Words are separated by a **single space**.  

The algorithm calculates:  
1. The **length of the sentence** (number of characters).  
2. The **number of words**.  
3. The **number of vowels**.

---

## ⚙️ Features
- Processes each character individually.  
- Uses **three counters** for characters, words, and vowels.  
- Handles spaces and tabs correctly to avoid counting extra words.  
- Treats vowels in both uppercase and lowercase (`a, e, i, o, u, y`).  
- Provides clear output for learning and understanding algorithm design.  

---

## 📝 Algorithm Documentation

### **Variables**
- `sentence` : STRING — the input sentence  
- `sentence_length` : INTEGER — counts total characters  
- `number_of_words` : INTEGER — counts words in the sentence  
- `number_of_vowels` : INTEGER — counts vowels  
- `vowels_list` : STRING — list of vowels (`aeiouyAEIOUY`)  
- `alphabet` : STRING — list of uppercase letters for validation  
- `char` : CHAR — current character being analyzed  
- `i, j` : INTEGER — loop indices  

---

### **Algorithm Steps**
1. **Initialize counters**: `sentence_length`, `number_of_words`, `number_of_vowels` → 0  
2. **Read the input sentence** from the user.  
3. **Validate input**:  
   - Sentence must not be empty  
   - First character must be uppercase  
   - Sentence must end with a period `.`  
4. **Iterate through each character** of the sentence:
   - Increment `sentence_length` for each character.  
   - If a **space, newline, or tab** is followed by a non-space and not a period, increment `number_of_words`.  
   - Check if the character is in `vowels_list`; if yes, increment `number_of_vowels`.  
5. **Increment `number_of_words` by 1** at the end to count the last word.  
6. **Output results**: sentence length, number of words, number of vowels.

---

### **Example Input and Output**
**Input:**  
Hello world.


**Step-by-step Analysis:**  
- Sentence length: 12 (including the space and excluding the period counted as character).  
- Words: 2 (`Hello` and `world`).  
- Vowels: 3 (`e, o, o`).  

**Output:**  
Length: 12
Words: 2
Vowels: 3