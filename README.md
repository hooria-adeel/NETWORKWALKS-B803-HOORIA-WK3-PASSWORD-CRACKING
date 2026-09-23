# NETWORKWALKS-B803-HOORIA-WK3-PASSWORD-CRACKING

## 📌 Overview
This repository contains my **Week 3** submission for the Cybersecurity & Ethical Hacking Internship at **Networkwalks Academy**.

The task focused on **password cracking of locked PDF files** using two different approaches:

- **Task A:** Cracking locked PDF passwords using **John the Ripper (JTR)** — both the command-line tool and its GUI front-end, **Johnny** — on Windows.
- **Task B:** Extracting the PDF hash and cracking it using Networkwalks' own browser-based tools — **Hash Calculator** and **Password Cracker** (dictionary attack) — no installation required.

Three locked PDFs were cracked in total across the two tasks.

---

## 🛠️ Tools Used
| Tool | Purpose |
|---|---|
| John the Ripper (JTR) | Command-line password cracking |
| Johnny | GUI front-end for JTR |
| Networkwalks Hash Calculator | Extracts `$pdf$` hash from a locked PDF |
| Networkwalks Password Cracker | Browser-based dictionary attack on the extracted hash |

---

## 🧩 Steps Followed

### Task A — JTR + Johnny (Locked PDF 1)
1. Located the locked PDF (`My Locked PDF1.pdf`) on Windows.
2. Extracted the PDF hash using `pdf2john`.
3. Opened **Johnny** (GUI for John the Ripper), loaded the password file/hash.
4. Ran the attack — Johnny matched the hash against a wordlist.
5. **Result:** Password successfully cracked → **`good-luck`**
6. Confirmed the crack by unlocking the PDF with the recovered password — flag captured.

### Task B — Networkwalks Hash Calculator + Password Cracker (Locked PDFs 2 & 3)
1. Uploaded the locked PDF to the **Hash Calculator** to extract its `$pdf$...` hash — no installation needed, fully browser-based.
2. Copied the extracted hash into the **Password Cracker** tool.
3. Ran the dictionary attack — tool tried wordlist entries sequentially (e.g. `service`, `canada`, `hockey`, `qwertyuiop`, `111222` ...) until a match was found.
4. **Locked PDF 2 result:** Password cracked → **`password1`**
5. **Locked PDF 3 result:** Password cracked → **`1qaz2wsx`** (alphanumeric password)
6. Opened each PDF with its respective recovered password to confirm — flags captured.

---

## 📸 Screenshots
| # | File | Description |
|---|---|---|
| 1 | `unlocked1.PNG` | Flag 1 captured — Locked PDF unlocked |
| 2 | `johntheripper.PNG` | Johnny GUI — hash loaded, password cracked (`good-luck`) |
| 3 | `unlockedpdf2.PNG` | Flag captured via JTR — persistence flag |
| 4 | `unlocked3.PNG` | Flag captured — Networkwalks tool completion |
| 5 | `pw_pdf3.png` | Networkwalks Password Cracker — dictionary attack in progress, password cracked (`1qaz2wsx`) |
| 6 | `pw_pdf2.png` | Networkwalks Password Cracker — match found, password cracked (`password1`) |

---

## 🔑 Cracked Passwords Summary
| PDF | Method | Password |
|---|---|---|
| Locked PDF 1 | John the Ripper (Johnny GUI) | `good-luck` |
| Locked PDF 2 | Networkwalks Password Cracker | `password1` |
| Locked PDF 3 | Networkwalks Password Cracker | `1qaz2wsx` |

---

## 🚩 Flags Captured
- `nw{cybersecurity_flag_captured_2608}`
- `nw{networkwalks_persistence_jtr_270521}`
- `nw{networkwalks_flag_260821_1}`

---

## 🧠 Key Learnings
- Learned how to extract crackable hashes from password-protected PDFs using `pdf2john`.
- Understood the difference between using JTR via command-line vs. its GUI (Johnny) — same engine, different workflow.
- Practiced dictionary attacks and saw firsthand how weak/common passwords (`password1`, `good-luck`) fall quickly, while even simple alphanumeric ones (`1qaz2wsx`) are only marginally harder.
- Reinforced why strong, non-dictionary-based passwords matter — every cracked password here came straight out of a common wordlist.
- Got comfortable with both installed security tools and browser-based alternatives for the same task.

---

## ⚠️ Disclaimer
This project was completed strictly for **educational purposes** as part of the Networkwalks Academy Cybersecurity & Ethical Hacking Internship. All PDFs, passwords, and hashes used belong to lab material provided by Networkwalks. No unauthorized access, cracking, or testing was performed on any real-world or third-party systems.
