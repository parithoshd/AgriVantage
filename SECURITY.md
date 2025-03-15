# Security Policy

## 🛡️ Supported Versions
We actively maintain and support the latest stable version of **AgriVantage**. Security updates will be provided for the latest release. Older versions may not receive security fixes.

| Version   | Supported          |
|-----------|--------------------|
| Latest    | ✅ Supported       |
| Older     | ❌ Not Supported   |

## 📢 Reporting a Vulnerability
If you discover a security vulnerability in **AgriVantage**, please follow these steps:

1. **Do not report the issue publicly.**
2. Contact the project maintainers **privately** via [parithoshdharmapalan@gmail.com] or open a **private** security report on GitHub.
3. Provide a clear and detailed description of the vulnerability, including:
   - Steps to reproduce the issue
   - Potential impact
   - Any suggested fixes
4. We will acknowledge your report within **48 hours** and work on a resolution.
5. Once a fix is implemented, we will release a security patch and notify the community.

## 🔐 Security Best Practices
To ensure a secure deployment of **AgriVantage**, follow these recommendations:

- **Keep dependencies updated** by running:
  ```sh
  pip install --upgrade -r requirements.txt
  ```
- Use **strong API keys** and never expose them in public repositories.
- Regularly rotate **Twilio, OpenAI, and ngrok** authentication tokens.
- Restrict **API access** to trusted sources.
- Enable **firewall rules** to limit unauthorized traffic.
- Avoid storing sensitive information in logs.

## ⏳ Response Timeline
- Acknowledgment of report: **48 hours**
- Investigation and fix: **1-2 weeks**, depending on complexity
- Security patch release: **As soon as possible**

Thank you for helping keep **AgriVantage** secure! 🛡️🚀
