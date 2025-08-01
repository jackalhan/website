# Company Logos

This directory contains company logos that will be displayed in the "experience" section of the about page.

## Adding Company Logos

1. Add your company logo image files to this directory
2. Update the `company_logos` section in `_config.yml` with the following format:

```yaml
company_logos:
  - name: "Company Name"
    logo: "company-logo-file.svg" # or .png, .jpg
    url: "https://company-website.com" # optional
    show_name: false # set to true to show company name below logo
```

## Image Guidelines

- **Preferred format**: SVG for scalability
- **Alternative formats**: PNG or JPG
- **Recommended size**: 120px width, 60px height (or similar aspect ratio)
- **Background**: Transparent or white background works best
- The logos will be displayed in grayscale by default and show color on hover

## Current logos:

- walmart-logo.svg (placeholder)
- google-logo.svg (placeholder)
- uark-logo.svg (placeholder)

Replace these placeholder files with actual company logos.
