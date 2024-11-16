# Swiss Climate Challenge Shutdown Page

This project contains the static shutdown page for the **Swiss Climate Challenge**. It will be published after the official shutdown, starting from **December 2nd, 2024**.

## Features

- **Language Support**: The shutdown page supports four languages (English, German, French, and Italian).
- **Hosted on GitHub Pages**: The shutdown page is statically hosted on GitHub Pages.
- **DNS and Domain**: The page will be published under the subdomain [app.swissclimatechallenge.ch](https://app.swissclimatechallenge.ch/).

## Language Support

The page is available in the following languages:

- **English (default)**
- **German**
- **French**
- **Italian**

Language selection is determined either by:

- The user's browser settings.
- The `userLang` parameter passed in the URL.

## Deployment

This project is deployed using GitHub Pages, under the NGTI organisation account. The DNS records for swissclimatechallenge.ch are managed by <dns.admin@swisscom.com>.

The DNS record must be configured as follows to point the `app.swissclimatechallenge.ch` subdomain to GitHub Pages:

- **Type**: `CNAME`
- **Name**: `app.swissclimatechallenge.ch`
- **Value**: `ngti.github.io`

To point the `swissclimatechallenge.ch` apex domain to GitHub Pages, follow the instructions in [Manage a custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Usage Instructions

The page is meant for Swiss Climate Challenge mobile clients (iOS and Android) and replaces the web application that provides the application UI.

- **Location**: The page is accessed at [app.swissclimatechallenge.ch](https://app.swissclimatechallenge.ch/).
- **Languages**: By default, the page will display in English, or in the browsers preferred language if it matches the languages available. The mobile client app can pass the language code (`userLang`) in the URL to override this.
  - Example: `https://app.swissclimatechallenge.ch/?userLang=de` will display the German version of the page.

## Local Development

1. **Clone the Repository**:

   ```sh
   git clone https://github.com/ngti/scc-static.git
   cd scc-static
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
