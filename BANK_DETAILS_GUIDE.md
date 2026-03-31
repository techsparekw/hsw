# Bank Details & Payment Information - Quick Reference

## Current Bank Details (Sample Data)

### 🏦 Bank Transfer
- **Bank Name**: State Bank of India (SBI)
- **Account Holder**: Al-Ehsan Muslim Orphanage
- **Account Number**: 35642189021845
- **IFSC Code**: SBIN0001234
- **Branch**: Kadapa, Andhra Pradesh

### 💳 Online Payment (UPI)
- **UPI ID**: haleemasadiya@sbi
- **Google Pay / PhonePe**: +91-8562-250885
- **Registered As**: 80(G) Approved Charity

### 🌍 International Transfer
- **SWIFT Code**: SBININBB143
- **Correspondent Bank**: JP Morgan Chase, USA
- **Bank Address**: State Bank of India, Kadapa Branch
- **Processing Time**: 3-5 Business Days

---

## How to Update Bank Details

### Step 1: Locate the Bank Details Section in HTML
Find the section starting with:
```html
<!-- BANK DETAILS -->
<section class="bank-details-section" id="bank-details">
```

### Step 2: Update Account Information

#### For Bank Transfer Card:
```html
<!-- REPLACE THESE VALUES -->
<div class="bank-details-value">State Bank of India (SBI)</div>
<!-- Change "State Bank of India (SBI)" to your actual bank -->

<div class="bank-details-value">Al-Ehsan Muslim Orphanage</div>
<!-- Change to your account holder name -->

<div class="bank-details-value">35642189021845</div>
<!-- Change to your account number -->

<div class="bank-details-value">SBIN0001234</div>
<!-- Change to your IFSC code -->

<div class="bank-details-value">Kadapa, Andhra Pradesh</div>
<!-- Change to your branch location -->
```

#### For Online Payment Card:
```html
<div class="bank-details-value">haleemasadiya@sbi</div>
<!-- Change to your UPI ID -->

<div class="bank-details-value">+91-8562-250885</div>
<!-- Change to your phone number for Google Pay/PhonePe -->
```

#### For International Transfer Card:
```html
<div class="bank-details-value">SBININBB143</div>
<!-- Change to your SWIFT code -->

<div class="bank-details-value">JP Morgan Chase, USA</div>
<!-- Change to your correspondent bank -->
```

### Step 3: Verify Copy Button Functionality

Each bank detail value should have an onclick attribute:
```html
<button class="copy-btn" onclick="copyToClipboard('YOUR_VALUE_HERE', this)">Copy</button>
```

Make sure the value in `copyToClipboard('...')` matches the bank detail value exactly.

### Step 4: Update Contact Information (Optional)

Find this line and update with your contact number:
```html
<span>Please mention 'Donation' in the reference/description field during transfer. 
All donations are 80(G) tax-exempt. For any queries, contact us at +91-8562-250885</span>
```

---

## Gallery Categories - Quick Reference

### Available Categories:
1. **daily-life** - Morning Routine, Meal Time, Recreation Time
2. **education** - Quranic Studies, Classroom Learning, Library Time
3. **activities** - Sports & Games, Art & Craft, Music & Culture
4. **events** - Eid Celebration, Ramadan Month, Annual Gathering
5. **vocational** - Sewing & Tailoring, Computer Training, Beauty & Care Training

### Adding New Gallery Images:

```html
<div class="gallery-item" data-category="CATEGORY_NAME" data-filter="CATEGORY_NAME,all">
  <img src="YOUR_IMAGE_URL" alt="Image Description">
  <div class="gallery-item-overlay">
    <span data-en="English Title" data-te="తెలుగు శీర్షిక" data-ar="العنوان بالعربية">English Title</span>
    <div class="gallery-item-category" data-en="Category" data-te="విభాగం" data-ar="الفئة">Category</div>
  </div>
</div>
```

---

## Important Notes

### Tax Exemption
✅ All donations are 80(G) tax-exempt
- Ensure this is clearly stated on the website
- Update if tax status changes
- Keep documentation for legal compliance

### Language Support
✅ All bank details support three languages:
- English (EN)
- Telugu (TE)  
- Arabic (AR)

When adding or updating information, include translations:
```html
<span data-en="English" data-te="తెలుగు" data-ar="العربية">English</span>
```

### Copy Button Functionality
✅ Copy buttons use the Clipboard API
- Modern browsers only (IE11 not supported)
- No external dependencies
- Shows "✓ Copied!" confirmation for 2 seconds
- Automatically reverts to "Copy" text

---

## Testing Your Updates

### Checklist:
- [ ] All bank detail values updated correctly
- [ ] Copy buttons work for each field
- [ ] Contact number is accurate
- [ ] No HTML syntax errors
- [ ] Test on desktop browser
- [ ] Test on mobile browser
- [ ] Language switching works (if applicable)
- [ ] Images display correctly
- [ ] No console errors (F12 Developer Tools)

---

## Troubleshooting

### Copy Button Not Working?
- Check browser compatibility (modern version required)
- Ensure JavaScript is enabled
- Clear browser cache and refresh
- Check console for errors (F12)

### Bank Details Not Showing?
- Check HTML syntax (matching quotes, tags)
- Verify section is not hidden with CSS
- Check that `id="bank-details"` exists
- Look for JavaScript errors in console

### Images Not Loading?
- Verify image URL is correct and accessible
- Check file permissions
- Use absolute URLs (starting with http:// or https://)
- Test image URL in browser address bar

### Multilingual Issues?
- Ensure all three data attributes are present
- Check language button is triggering correctly
- Clear browser cache
- Test each language separately

---

## Security Tips

### For Donation Information:
1. **Use HTTPS** - Ensure website uses SSL certificate
2. **Don't Store Sensitive Data** - Never log actual account numbers in frontend
3. **Validate Input** - Server should validate donation references
4. **Regular Backups** - Backup website files regularly
5. **Monitor Transactions** - Keep track of donations received

### For Images:
1. **Use CDN** - Consider content delivery network for images
2. **Compress Images** - Reduce file size without losing quality
3. **Copyright Check** - Ensure all images are properly licensed
4. **Alt Text** - All images must have descriptive alt text (accessibility)

---

## Mobile-Specific Considerations

### On Mobile Devices:
- Copy buttons work with Clipboard API
- Three-column layout becomes single column
- Images remain optimized for smaller screens
- Touch-friendly button sizes (48px minimum)
- All filters remain functional

### Testing on Mobile:
- Test on actual devices (not just desktop emulation)
- Test all filter buttons
- Test copy functionality with mobile keyboards
- Verify responsive layout breaks correctly

---

## Analytics Recommendations

To track donations, consider adding:
1. **UTM Parameters** - Track donation source in links
2. **Google Analytics Events** - Track copy button clicks
3. **Conversion Tracking** - Monitor donation page visits
4. **Form Analytics** - If you add a donation form

### Example UTM Link:
```
https://yoursite.com#bank-details?utm_source=email&utm_medium=newsletter&utm_campaign=Q1_2026
```

---

## Frequently Asked Questions (FAQ)

### Q: Can I add more payment methods?
A: Yes! You can add more cards by duplicating the `.bank-card` div and updating the content.

### Q: Can I change the number of columns?
A: Yes! Modify `grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));` in CSS to change layout.

### Q: Can I change the colors?
A: Yes! Update the CSS color variables:
- Primary: `--emerald`, `--emerald-light`
- Accent: `--gold`, `--gold-light`
- Backgrounds: `--cream`, `--dark`

### Q: How do I add a new gallery category?
A: Add a new filter button and use the category name in `data-category` and `data-filter` attributes.

### Q: Will copy buttons work on all devices?
A: Yes, but requires modern browsers (Chrome, Firefox, Safari, Edge). IE11 not supported.

---

## Contact Information Update

Current contact number: **+91-8562-250885**

To update, find and replace this number in:
1. Bank Details Section (under "Important Information" box)
2. Navigation → Contact Links
3. Footer Contact Information
4. Any other hardcoded numbers

---

**Last Updated**: March 31, 2026
**Version**: 1.0
