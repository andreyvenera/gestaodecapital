# Gestão de Capital

**Personal Capital Management** by Nectar Ventures

A personal wealth app to track bank accounts in multiple currencies, real estate, installments and receivables, follow wealth goals with a progress bar, and get live USD and CDI rates every day.

🔗 **Live app** · [andreyvenera.github.io/gestaodecapital](https://andreyvenera.github.io/gestaodecapital/)

---

## Features

**Accounts and currencies**
Balances in 13 currencies (BRL, USD, EUR, GBP, CAD, AUD, CHF, JPY, CNY, ARS, MXN, CLP and BTC), converted at the daily rate, with a quick toggle to view everything in reais or dollars.

**Real estate**
Each property has its own card with address, Google Maps link, down payment, installments, amount paid, outstanding balance, estimated sale value and automatic return %.

**Calendar**
Every entry goes on the calendar. Paying an installment updates the property on its own, and past balances can be edited month by month.

**Receivables**
Track money owed to you by person, currency and expected date, with totals and a projection of your balance once everything is received.

**Goals**
Three editable goals (liquidity, real estate and total net worth) with an animated progress bar, 25/50/75% milestones and a forecast of when you reach your first million.

**Dashboard**
Total net worth, liquidity, real estate, monthly CDI income, a wealth evolution chart, and a portfolio breakdown.

**Achievements and Our Story**
Achievements grouped by topic, plus a timeline of moments, properties and milestones.

**Privacy mode**
One tap hides every amount, percentage, chart and achievement that could hint at your numbers.

**Simple mode**
A clean view with just what matters: how much you have, how much is left and how much you grew this month.

**Accounts with username and PIN**
Anyone can create an account. Each account's data is stored separately and protected by a PIN.

**6 languages on the sign in screen**
English, Português, 中文, Lëtzebuergesch, Français and Deutsch.

---

## Tech

| Part | Stack |
|---|---|
| Front end | A single `index.html` file (HTML, CSS and JavaScript, no build step) hosted on GitHub Pages |
| Back end | Google Apps Script web app (`Code.gs`) |
| Database | Google Sheets, one tab per account |
| Rates | AwesomeAPI and ExchangeRate API for currencies, Banco Central do Brasil for CDI |

PINs are never stored in plain text. Only a SHA-256 hash is saved, sessions use signed tokens, and too many wrong attempts lock the account for 10 minutes.

---

## Run your own copy

1. Create a new Google Sheet.
2. Open **Extensions → Apps Script** and paste the content of `Code.gs`.
3. Run the `autorizar` function once and accept the permissions.
4. Go to **Deploy → New deployment → Web app**, set **Execute as Me** and **Who has access Anyone**, then deploy.
5. Copy the URL ending in `/exec` and paste it into `API_URL` at the top of the script in `index.html`.
6. Upload `index.html` to a GitHub repository and turn on **GitHub Pages**.

Whenever `Code.gs` changes, edit the existing deployment and choose **New version** so the URL stays the same.

---

## Contact

[amarques.xyz](https://amarques.xyz/)

---

© 2026 Andrey Marques. All rights reserved.
For personal financial management and record-keeping purposes only.
