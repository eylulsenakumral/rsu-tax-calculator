# RSU Tax Calculator 🚀

**Free, open-source tax calculator for tech workers with RSUs and ISOs.**

> 💡 **Live Demo:** https://eylulsenakumral.github.io/rsu-tax-calculator/

> ⚠️ **DISCLAIMER: This calculator is for educational purposes only and does not constitute tax, legal, or financial advice. Consult a qualified tax professional for your specific situation.**

[![Stars](https://img.shields.io/github/stars/eylulsenakumral/rsu-tax-calculator?style=social)](https://github.com/eylulsenakumral/rsu-tax-calculator)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 💡 Why I Built This

I overpaid **$3,200** in RSU taxes last year because I sold at the wrong time. The frustrating part? No tool showed me the impact of different sell strategies before I made the decision.

So I built what I wished existed.

## ✨ Features

- ✅ **Strategy Comparison** - "Sell now" vs "sell later" with actual tax numbers
- ✅ **Tax Bracket Visualization** - See exactly how your income is taxed
- ✅ **AMT Exposure** - ISO holders can see AMT hit before exercising
- ✅ **Vesting Schedules** - Model based on your actual cliff dates
- ✅ **Print/PDF Export** - Save calculations for your records

## 📊 Live Demo

Visit **https://eylulsenakumral.github.io/rsu-tax-calculator/**

No signup required. All calculations happen in your browser.

## 💰 Pricing

| Tier | Price | Features |
|------|-------|----------|
| **Free** | $0 | Basic modeling, single scenario |
| **Report** | $9 | One-time decision analysis |
| **Monthly** | $19/month | Full features, ongoing optimization |
| **Lifetime** | $149 | One-time purchase, forever access |

## 🛠 Tech Stack

- **Framework:** Next.js 16.2.7 (App Router, React Server Components)
- **Runtime:** React 19
- **Styling:** Tailwind CSS 4
- **Charts:** Recharts
- **Tax Engine:** Custom TypeScript (pure functions, 100% testable)

## 🚀 Quick Start

### Use Live Demo
https://eylulsenakumral.github.io/rsu-tax-calculator/

### Run Locally
\`\`\`bash
# Install dependencies
npm install

# Run development server
npm run dev

# Open http://localhost:3000
\`\`\`

## 📈 Tax Year: 2025

This calculator uses the latest 2025 IRS tax brackets:

| Rate | Single (min-max) | MFJ (min-max) |
|------|------------------|---------------|
| 10%  | $0 - $11,600     | $0 - $23,200  |
| 12%  | $11,600 - $47,150 | $23,200 - $94,300 |
| 22%  | $47,150 - $100,525 | $94,300 - $201,050 |
| 24%  | $100,525 - $191,950 | $201,050 - $383,900 |
| 32%  | $191,950 - $243,725 | $383,900 - $487,450 |
| 35%  | $243,725 - $609,350 | $487,450 - $731,200 |
| 37%  | $609,350+        | $731,200+     |

**Standard Deductions:**
- Single: $14,600
- MFJ: $29,200
- HOH: $21,800

## 🔧 Build & Deploy

\`\`\`bash
# Build for production
npm run build

# Start production server
npm start
\`\`\`

### GitHub Pages Deployment
This project is deployed to GitHub Pages:
- **Repo:** https://github.com/eylulsenakumral/rsu-tax-calculator
- **Live:** https://eylulsenakumral.github.io/rsu-tax-calculator/

## 📝 API

### POST /api/calculate

Calculate tax for a single scenario:

\`\`\`json
{
  "shares": 100,
  "vestPrice": 50,
  "sellPrice": 60,
  "otherIncome": 100000,
  "filingStatus": "SINGLE",
  "compare": false
}
\`\`\`

Response:
\`\`\`json
{
  "proceeds": 6000,
  "ordinaryTax": 0,
  "capitalGainsTax": 225,
  "totalTax": 225,
  "netProceeds": 5775,
  "effectiveRate": 0.0375,
  "year": 2025,
  "holdingPeriod": "SHORT"
}
\`\`\`

## 🤝 Contributing

Found a bug? Have a feature request? 
- Open an issue: https://github.com/eylulsenakumral/rsu-tax-calculator/issues
- PRs welcome!

## 📄 License

MIT License - Free for personal and commercial use.

## 🔔 Updates

Tax brackets and standard deductions are updated annually. Star the repo to get notified.

---

**Built with 2025 IRS data. Last updated: June 2025**

**Questions?** Check the [Discussions](https://github.com/eylulsenakumral/rsu-tax-calculator/discussions) or open an issue.
