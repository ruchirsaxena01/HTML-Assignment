# Assignment 1 – What happens between typing a URL and seeing the page?

When I type a URL (such as `https://www.invertisuniversity.ac.in`) into my browser and hit Enter, a series of network requests and rendering steps take place in fractions of a second:

1. **URL Parsing & Cache Inspection:**
   The browser parses the protocol (`https://`), domain name, and path. It checks multiple layers of cache (browser cache, operating system cache, and router cache) to see if the IP address for the domain is already stored locally.

2. **DNS Resolution (Domain Name System):**
   If the IP address is not cached, the browser queries a recursive DNS resolver (usually provided by the ISP or a public DNS like 8.8.8.8). The resolver queries the Root server (`.`), the Top-Level Domain (TLD) server (`.in` / `.ac.in`), and finally the Authoritative Name Server to get the exact IPv4 or IPv6 address.

3. **TCP Connection & TLS Handshake:**
   The browser establishes a TCP connection to the destination server using a three-way handshake (SYN, SYN-ACK, ACK). Because HTTPS is used, an additional TLS/SSL handshake occurs to negotiate encryption ciphers, exchange keys, and verify the server's SSL certificate.

4. **HTTP Request & Server Processing:**
   The browser sends an HTTP `GET` request containing headers like `User-Agent`, `Accept`, and cookies. The web server (e.g. Nginx, Apache) processes the request and returns an HTTP response code (e.g. `200 OK`) along with the HTML document payload.

5. **Parsing and Building Trees:**
   - **DOM Tree:** The browser parses raw HTML bytes into characters, tokens, nodes, and finally constructs the Document Object Model (DOM).
   - **CSSOM Tree:** While parsing, the browser encounters `<link rel="stylesheet">` or `<style>` tags and parses CSS rules into the CSS Object Model (CSSOM).

6. **Render Tree & Layout (Reflow):**
   The browser combines the visible DOM nodes with CSSOM rules to create the **Render Tree** (nodes with `display: none` or `<head>` are omitted). Next, the **Layout** stage computes the exact geometry, coordinates, width, and height of every element on the screen.

7. **Painting & Compositing:**
   During the **Paint** stage, pixels are drawn to the screen (backgrounds, borders, text, shadows). The **Compositor** organizes these layers and coordinates with the GPU to display the final page smoothly. If JavaScript is downloaded and run, it can modify the DOM or CSSOM, triggering repaints or reflows.
