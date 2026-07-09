# 🔐 Password Strength Checker

A tool that evaluates a password as you type it and classifies it as **Weak**, **Medium**, or **Strong**, based on length and character variety — giving instant, actionable feedback instead of a vague "password too weak" message after submission.

> 🔗 **Live demo:** `<sakshipatel-07>` 
> `https://<sakshipatel-07>.github.io/password-strength-checker/`

---

## ✨ Features

- ✅ Real-time validation — updates on every keystroke, no submit button needed
- 📊 Live 0–100% strength score
- 🎨 Color-coded strength meter (🔴 red / 🟡 yellow / 🟢 green)
- 📋 Checklist showing exactly which requirements are met (✓) or missing (✗)
- 💡 Plain-language suggestions to improve a weak password
- 🙈 Password field is masked by default, with a Show/Hide toggle
- 🔒 Fully client-side — the password never leaves your browser/device

---

## 📏 Rules

**Minimum length:** 8 characters

**Character types checked (via regex):**
- Uppercase letters (`A–Z`)
- Lowercase letters (`a–z`)
- Numbers (`0–9`)
- Special characters: `@ # $ % & * ! ? _ - + = ^ ( ) [ ] { } : ; , . < > / \ | ~`

**Strength classification:**

| Strength | Criteria |
|---|---|
| 🔴 Weak | Under 8 characters, or only 1 character type present |
| 🟡 Medium | 8+ characters with 2–3 character types |
| 🟢 Strong | 8+ characters with all 4 character types (bonus if 12+) |

---

## 🖥️ Two versions included

### 1. Web app (HTML / CSS / JavaScript)
Runs directly in any browser — no install needed.

**To use it:**
1. Open `password-strength-checker.html` in any browser (just double-click it), **or**
2. Deploy it via GitHub Pages for a live shareable link (see below)

### 2. Python app (CLI + Tkinter GUI)
Same logic and rules, running locally.

**To use the terminal version:**
```bash
pip install colorama
python password_strength_checker.py
```

**To use the desktop GUI version** (no extra install needed — uses Python's built-in `tkinter`):
```bash
python password_strength_checker_gui.py
```

---

## 📂 Project structure

```
password-strength-checker/
├── index.html                          # Web version (rename from password-strength-checker.html)
└── README.md
```

---

## 🚀 Deploying the web version with GitHub Pages

1. Rename `password-strength-checker.html` to `index.html`
2. Push it to this repository
3. Go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch** → branch `main`, folder `/ (root)` → **Save**
5. After about a minute, your live link will appear at the top of that Pages settings screen

---

## 🛡️ Security concepts demonstrated

- Character-class enforcement (regex-based password composition policy)
- Length-based brute-force resistance
- Masked password input (`type="password"`)
- Disabled autofill/autocomplete caching
- Fully client-side processing — no network calls, no data transmission

> **Note:** This is a client-side strength *indicator*, meant for UX and education. It is not a substitute for server-side validation and secure password hashing (e.g. bcrypt/Argon2) in a real authentication system.

---

## 🧰 Tech stack

- HTML5, CSS3, vanilla JavaScript (web version)
- Python 3 + `re` (regex) + `tkinter` (Python versions)
- Optional: `colorama` for the CLI's colored output

---

## 📄 License

Feel free to use, modify, and share this project. Add a license of your choice (e.g. MIT) here if you plan to open-source it.
