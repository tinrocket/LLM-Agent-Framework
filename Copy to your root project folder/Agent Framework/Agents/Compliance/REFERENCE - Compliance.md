# Compliance — Reference

Asset tracking templates, license guides, and escalation triggers.

---

## Areas of Focus

### Asset Tracking
For every asset used (images, audio, fonts, code libraries, etc.):
- Source: Where did it come from?
- License: What are the terms?
- Attribution: What notices are required?
- Restrictions: What can't we do with it?

### License Inventory
Maintain a record of all licenses in use:
- Open source licenses (MIT, GPL, Apache, etc.)
- Commercial licenses
- Royalty-free vs. rights-managed assets
- License compatibility issues

### Required Notices
Track what must be published or displayed:
- Attribution requirements
- License texts that must be included
- Privacy policy requirements
- Terms of service needs
- Cookie/tracking disclosures

### Regulatory Awareness
Flag when the project may touch regulated areas:
- Data protection (GDPR, CCPA, etc.)
- Accessibility requirements
- Age restrictions or ratings
- Export controls
- Industry-specific regulations
- Algorithm restrictions (e.g., AI/ML regulations)

**Note:** Research and flag these issues — do not interpret legal requirements. Recommend consulting appropriate legal counsel.

---

## Asset Record Template

```markdown
## [Asset Name]
- **Type:** Image / Audio / Font / Code Library / etc.
- **Source:** [Where obtained]
- **License:** [License type]
- **Attribution Required:** Yes / No
- **Attribution Text:** [Exact text if required]
- **Restrictions:** [What we can't do]
- **Expiration:** [If applicable]
- **Notes:** [Anything else relevant]
```

---

## Red Flags to Escalate

Always flag for human/legal review:
- Unclear or missing license information
- GPL or other copyleft in commercial product
- User data crossing international borders
- AI/ML training data sources
- Anything involving children's data
- Healthcare or financial data
- Assets with "no commercial use" restrictions being used commercially
