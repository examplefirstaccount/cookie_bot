### Cookie Collecting Robot

---

#### Overview

This project is a Python-based "Cookie Collecting Robot" designed to collect cookies from a list of top websites, either globally or specific to a country. The script uses Playwright, an end-to-end testing and automation framework, to open web pages in a headless browser and gather cookies. The collected cookies can be saved to a file for further analysis or use.

#### Features

- **Country Detection:** Detects the country based on the provided IP address. Bot uses your IP address if no IP provided. 
- **Top Websites Fetching:** Fetches a list of top websites using SimilarWeb, either globally or specific to a country. (limit: top-50)
- **Cookie Collection:** Collects cookies from these websites using a headless browser.
- **Proxy Support:** Supports the use of a proxy server during the cookie collection process. (almost)
- **Customizable Options:** Allows customization for the number of websites, max browser tabs, headless mode, and randomization.

---

#### Requirements

- Python 3.7+
- Playwright
- requests

#### Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/examplefirstaccount/cookie_bot.git
   cd cookie-bot
   ```

2. **Install Dependencies:**
   Ensure you have Python 3.7+ installed, then install the required Python packages:
   ```bash
   pip install playwright requests
   ```

3. **Set Up Playwright:**
   Install Playwright's browsers:
   ```bash
   playwright install
   ```

#### Usage

1. **Basic Usage:**

   The script can be run directly, and it will automatically detect the country based on the provided IP address, fetch the top websites for that country, and start collecting cookies.

   ```bash
   python cookie_robot.py
   ```

   The script will save the collected cookies to a file named `cookies.txt`.

2. **Using a Proxy:**

   You can specify a proxy by passing a `Proxy` object to the `main` function. Here is an example:
   ```python
   proxy = Proxy(host='192.92.191.91', port=64444, user='your_user', password='your_password')
   asyncio.run(main(proxy=proxy))
   ```

3. **Customizing Parameters:**

   - **IP Address:** You can provide a specific IP address to detect the country.
   - **Number of Websites:** Customize the number of websites to fetch and visit.
   - **Headless Mode:** Run the browser in headless mode or with a GUI.
   - **Max Tabs:** Set the maximum number of tabs to open simultaneously.

   Example:
   ```python
   asyncio.run(main(ip_address='192.168.1.1', proxy=proxy))
   ```

---

#### Future Enhancements

1. **Proxy Support:** Add proxy support for Playwright.
2. **Reusable Webdriver:** Improve performance by reusing the browser context across sessions.
3. **User-Agent Spoofing:** Implement user-agent spoofing to simulate different browsers.
4. **Category-Based Website Collection:** Allow fetching websites by categories.
5. **Randomization:** Add options for randomizing categories, the number of sites, and other parameters.

