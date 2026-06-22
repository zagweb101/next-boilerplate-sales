# Gumroad Setup Guide — Next Boilerplate

This guide walks you through setting up 3 products on Gumroad to sell the Next Boilerplate.

---

## Step 1: Create a Gumroad Account

1. Go to [gumroad.com](https://gumroad.com) and sign up
2. Complete your profile (name, email, payment info)
3. Set up your payout method (PayPal or bank transfer)

## Step 2: Create 3 Products

### Product 1: Single License ($79)

1. Click **"Add a product"** → **"Digital"**
2. Fill in:
   - **Name:** Next Boilerplate — Single License
   - **Price:** $79
   - **Description:** Production-ready Next.js 16 boilerplate. Use in 1 commercial project. Includes 18+ routes, auth, Stripe, teams, AI, and more.
3. Upload the deliverable (see Step 3 below)
4. Under **"Content"** tab, add the GitHub template repo link
5. Under **"Settings"**:
   - Enable **"Require a shipping address"** → No
   - Set **"Return URL"** to your sales page
6. Save and copy the product URL (e.g., `https://gumroad.com/l/abc123`)

### Product 2: Unlimited License ($199)

1. Same as above, but:
   - **Name:** Next Boilerplate — Unlimited License
   - **Price:** $199
   - **Description:** Use in unlimited commercial projects + client work. Lifetime updates. GitHub template access.
2. Upload the deliverable
3. Add a private GitHub repo invite link in the content
4. Save and copy the product URL

### Product 3: Pro License ($299)

1. Same as above, but:
   - **Name:** Next Boilerplate — Pro License
   - **Price:** $299
   - **Description:** Everything in Unlimited + 6 months support + private Discord + priority requests.
2. Upload the deliverable
3. Add Discord invite link + support email in the content
4. Save and copy the product URL

---

## Step 3: Prepare the Deliverable

For each product, the customer should receive after purchase:

```
Thank you for purchasing Next Boilerplate!

Here's what you get:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📥 GitHub Template Repo:
   https://github.com/zagweb101/next-boilerplate
   (Click "Use this template" to create your project)

📋 License Key: [GENERATED-KEY]

📄 License Agreement: [link to LICENSE.md]

🚀 Quick Start:
   1. Click "Use this template" on GitHub
   2. Clone your new repo
   3. Run: npm install
   4. Copy .env.example to .env and fill in your keys
   5. Run: npx prisma migrate dev
   6. Run: npm run dev

📖 Full documentation: [link to README]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Questions? Email: support@your-domain.com
```

### How to deliver:
- **Single License:** Upload a `.txt` or `.pdf` file with the above text as the product file
- **Unlimited/Pro:** Same + add the private repo/Discord links
- Gumroad will automatically send this to the buyer after payment

---

## Step 4: Update the Sales Landing Page

Replace the placeholder Gumroad links in `index.html`:

```html
<!-- Single License -->
<a href="https://gumroad.com/l/YOUR-SINGLE-LICENSE" class="buy secondary">Buy Now</a>

<!-- Unlimited License -->
<a href="https://gumroad.com/l/YOUR-UNLIMITED-LICENSE" class="buy primary">Buy Now</a>

<!-- Pro License -->
<a href="https://gumroad.com/l/YOUR-PRO-LICENSE" class="buy secondary">Buy Now</a>
```

Replace `YOUR-SINGLE-LICENSE`, `YOUR-UNLIMITED-LICENSE`, `YOUR-PRO-LICENSE` with the actual Gumroad product URLs from Step 2.

---

## Step 5: Deploy the Sales Page

### Option A: Vercel (recommended)
```bash
npx vercel
# Follow the prompts
```

### Option B: Netlify
```bash
npx netlify deploy
```

### Option C: GitHub Pages
1. Create a new repo called `next-boilerplate-sales`
2. Upload `index.html`
3. Enable GitHub Pages in repo settings

---

## Step 6: Set Up the GitHub Template Repo

### For Single License buyers:
- They receive a link to the public repo
- They can download it once and use it in 1 project

### For Unlimited/Pro License buyers:
1. Make the repo a **template repository**:
   - Go to repo Settings → check "Template repository"
2. Buyers click "Use this template" → new repo created
3. They can do this unlimited times

### Optional: Private repo for Pro buyers
- Create a private repo
- Add buyers as collaborators manually after purchase
- Or use GitHub Teams for bulk management

---

## Step 7: Launch Checklist

- [ ] Gumroad account created
- [ ] 3 products created ($79 / $199 / $299)
- [ ] Deliverable text uploaded to each product
- [ ] Sales page deployed (Vercel/Netlify)
- [ ] Gumroad links replaced in sales page
- [ ] GitHub repo set as template
- [ ] Demo deployed on Railway
- [ ] LICENSE.md added to repo
- [ ] ProductHunt launch prepared
- [ ] Twitter/X announcement ready

---

## Gumroad Fees

- **Free plan:** 10% per sale + payment processing fees
- **Premium plan ($10/mo):** Lower fees

### Revenue projection (at 10 sales/month):
| Product | Price | Sales/mo | Revenue |
|---------|-------|----------|---------|
| Single | $79 | 5 | $395 |
| Unlimited | $199 | 3 | $597 |
| Pro | $299 | 2 | $598 |
| **Total** | | **10** | **$1,590/mo** |
