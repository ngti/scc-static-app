# Swiss Climate Challenge Shutdown Page

This project contains the static shutdown page for the **Swiss Climate Challenge**. It will be published after the official shutdown, starting from **December 2nd, 2024**.

## Features

- **Language Support**: The shutdown page supports four languages (English, German, French, and Italian). The page content is selected based on the user's browser language or a query parameter (`userLang`) to override the default selection.
- **Hosted on GitHub Pages**: The shutdown page is statically hosted on GitHub Pages, under the NGTI account.
- **DNS and Domain**: The page will be published under the subdomain [app.swissclimatechallenge.ch](https://app.swissclimatechallenge.ch/). The DNS records are managed by <dns.admin@swisscom.com>

## Deployment

This project is deployed using GitHub Pages, and the DNS record must be configured as follows to point to GitHub Pages:

- **Type**: CNAME
- **Name**: app.swissclimatechallenge.ch
- **Value**: `ngti.github.io`

## Usage Instructions

- **Languages**: By default, the page will display in English. The mobile client app can pass the language code (`userLang`) in the URL to override this.
  - Example: `https://app.swissclimatechallenge.ch/?userLang=de` will display the German version of the page.

## Local Development

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/ngti/swissclimatechallenge-shutdown.git
   cd swissclimatechallenge-shutdown
   ```

2. **Serve Locally**:
   Use a simple HTTP server to view the page locally.

   ```sh
   python3 -m http.server
   ```

3. **Access the Page**:
   Visit `http://localhost:8000` in your browser.

## Folder Structure

- `index.html`: The main shutdown page HTML file.
- `scc-clouds.svg`: The SVG illustration used in the shutdown page.
- `fonts/`: Contains font files for the Swisscom version of TheSans (400 and 700 weights) used by the page.

## Language Support

The page is available in the following languages:

- **English (default)**
- **German**
- **French**
- **Italian**

Language selection is determined either by:

- The user's browser settings.
- The `userLang` parameter passed in the URL.
