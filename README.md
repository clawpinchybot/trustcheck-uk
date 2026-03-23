# TrustCheck UK - Tradesman Vetting Tool

**Status:** 🚧 MVP IN PROGRESS (started 2026-03-23)

---

## Problem

80% of UK homeowners don't trust tradesman platforms (Checkatrade, MyBuilder) due to:
- Fake reviews
- No real verification
- "Cowboy builders" with great platform ratings

**Evidence:** See `../OPPORTUNITY-TRADESMAN-VETTING-TOOL.md`

---

## Solution

Instant vetting report for UK tradesmen checking:
- Company status (active, dissolved, liquidation)
- Director history (previous dissolved companies)
- Filing compliance (accounts on time?)
- CCJs (county court judgments)
- Aggregated reviews

---

## MVP Approach

### Phase 1 (Current) - Manual Helper
**Goal:** Validate demand before investing in API integration

**Features:**
- Pre-filled search links to Companies House, TrustOnline, Google
- Printable verification checklist
- Red flag explanations
- "What to look for" guidance

**Why Manual?**
- Companies House API requires server-side proxy (API key can't be client-side)
- TrustOnline has NO public API
- Manual helper still saves 30+ minutes per check

**Value Proposition:**
- Current: 30+ minutes searching multiple sites
- With TrustCheck: 2 minutes following guided checklist

### Phase 2 - Automated (If Phase 1 Validates)
**Requirements:**
- Serverless backend (Vercel/Netlify/Render)
- Companies House API key (free)
- TrustOnline partnership OR affiliate link

**Features:**
- Automated company lookup
- Director history analysis
- One-click PDF report
- Pricing: £2.99/check or £9.99/3-pack

---

## Technical Notes

### Companies House API
- **URL:** `https://api.company-information.service.gov.uk`
- **Cost:** FREE
- **Rate Limit:** 600 requests/5 minutes
- **Issue:** Requires API key (can't be client-side)

### TrustOnline (CCJs)
- **URL:** `https://www.trustonline.org.uk`
- **Cost:** £4-10 per search
- **API:** ❌ NO PUBLIC API
- **Alternative:** Affiliate link or manual redirect

### Google Places API
- **Cost:** Free tier (200k calls/month)
- **Use:** Pull Google reviews automatically

---

## Files

- `index.html` - Main MVP interface
- `README.md` - This file

---

## Deployment

**Option 1: GitHub Pages** (Free, static only)
- No API integration
- Manual helper only
- Instant deployment

**Option 2: Vercel/Netlify** (Free tier)
- Serverless functions for API proxy
- Automated checks possible
- Slightly more complex

**Recommendation:** Start with GitHub Pages for Phase 1 validation.

---

## Next Steps

1. ✅ Create MVP interface (manual helper)
2. ⏳ Test with real tradesmen searches
3. ⏳ Deploy to GitHub Pages
4. ⏳ Post to r/DIYUK for feedback
5. ⏳ If positive response → Build Phase 2

---

## Success Metrics

**Phase 1 (Validation):**
- 100+ visits in first week
- 10+ positive comments on Reddit
- 5+ emails asking for automated version

**Phase 2 (Build):**
- 10 paid checks in first month
- £25+ revenue

---

*Started: 2026-03-23 01:45 UTC*
