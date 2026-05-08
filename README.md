# 🔐 Random Password Generator

A clean and minimal random password generator built with pure **HTML**, **CSS**, and **JavaScript** — instantly generates strong 12-character passwords with uppercase, lowercase, numbers, and symbols, with one-click copy support.

---

## 🖼️ Preview

![Password Generator Preview](preview.png)

---

## ✨ Features

- ⚡ Instantly generates a strong 12-character password
- 🔠 Includes uppercase, lowercase, numbers & symbols
- 🔀 Shuffled characters for true randomness
- 📋 One-click copy to clipboard
- 🎨 Dark navy & green minimal design
- 📱 Clean, responsive layout

---

## 📁 Project Structure

```
PasswordGenerator/
├── index.html        # Markup & structure
├── style.css         # Styling & layout
├── script.js         # Password generation & copy logic
├── preview.png       # Screenshot for README
└── images/
    ├── copy.png      # Copy icon
    └── generate.png  # Generate button icon
```

---

## 🚀 Getting Started

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-username/password-generator.git
   cd password-generator
   ```

2. **Open in browser**
   ```bash
   # No setup needed — just open index.html directly
   ```

---

## 🛠️ How It Works

The password is built by guaranteeing at least one character from each category, then filling the rest randomly from the combined character set. The final string is shuffled so the guaranteed characters don't always appear at the start.

```js
// Guarantee one of each type
password += upperCase[Math.floor(Math.random() * upperCase.length)];
password += lowerCase[Math.floor(Math.random() * lowerCase.length)];
password += number[Math.floor(Math.random() * number.length)];
password += symbol[Math.floor(Math.random() * symbol.length)];

// Fill remaining length from all characters
while (length > password.length) {
  password += allChars[Math.floor(Math.random() * allChars.length)];
}

// Shuffle so guaranteed chars aren't always first
passwordBox.value = shuffleString(password);
```

---

## 🛠️ Customization

### Change password length
In `script.js`, update the `length` variable:
```js
const length = 16; // default is 12
```

### Remove symbols from password
In `script.js`, remove `symbol` from `allChars`:
```js
const allChars = upperCase + lowerCase + number;
// and remove: password += symbol[...]
```

### Change accent color
In `style.css`, replace `#019f55` with your preferred color:
```css
.container h1 span { color: #019f55; border-bottom: 4px solid #019f55; }
.container button  { background: #019f55; }
```

---

## 🎨 Color Palette

| Element | Color |
|---------|-------|
| Background | `#002339` — Deep Navy |
| Accent | `#019f55` — Emerald Green |
| Text | `#ffffff` — White |
| Input background | `#ffffff` — White |

---

## 🙋‍♀️ Author

**Kaneeza Batool**
CS Undergraduate · Sukkur, Pakistan
Built with 🔐 using HTML, CSS & JS
