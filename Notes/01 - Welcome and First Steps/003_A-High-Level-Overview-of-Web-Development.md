# A High-Level Overview of Web Development

### Key Concepts/Overview

This overview introduces the fundamental concepts and terminology of web development. It explains the process that occurs when a user accesses a webpage, defines the roles of front-end and back-end development, and differentiates between static and dynamic websites. The main goal is to provide a foundational understanding of the web development landscape before learning to code.

---

### Detailed Breakdown

#### 1. The Webpage Request-Response Cycle

When you visit a website (e.g., `omnifood.dev`), a specific process happens between your computer (the client) and the website's host (the server).

-   **Client:** Your web browser (e.g., Chrome, Firefox).
-   **Server:** A computer connected to the internet that stores a website's files and is able to receive requests.

**The Process:**
1.  **Request:** Your browser (the **client**) sends a request to the **server** where the website is hosted.
2.  **Response:** The server receives the request, gathers all the files that make up the website (HTML, CSS, JavaScript), and sends them back to the browser in a **response**.
3.  **Render:** The browser receives these files, interprets the code, and **renders** the visual webpage for you to see.

#### 2. Front-End vs. Back-End Development

Web development is often split into two main areas: front-end and back-end.

##### **Front-End Development**

-   **Definition:** The process of writing code that the browser can understand and display. It is the **visible part** of a website that users interact with directly.
-   **Core Technologies:** The three core languages that all browsers understand are:
    1.  **HTML (HyperText Markup Language)**
    2.  **CSS (Cascading Style Sheets)**
    3.  **JavaScript (JS)**
-   **Focus:** Building the user interface and user experience.

##### **Back-End Development**

-   **Definition:** The "invisible" part of a website that runs on the server. It handles the logic, database interactions, and application performance.
-   **Core Technologies:** Involves server-side languages to process data and generate the files that are sent to the browser.
    -   *Examples:* Node.js, PHP, Python.
-   **Function:** Manages data from a **database** (which stores content like users, courses, reviews, etc.) and assembles it into the final files (HTML, CSS, JS) sent to the browser.

#### 3. Static vs. Dynamic Websites

The distinction between static and dynamic websites lies in how the content is stored and delivered from the server.

##### **Static Websites**

-   **Definition:** A website where the files (HTML, CSS, JS) are stored on the server and are sent to the browser **exactly as they are**.
-   **Characteristics:**
    -   The content does not change unless a developer manually updates the files on the server.
    -   The files are "pre-made" and waiting to be requested.
-   **Example:** The `omnifood.dev` project, a simple portfolio or informational site.

##### **Dynamic Websites**

-   **Definition:** A website where the content is **dynamically assembled on the server** each time a user visits.
-   **Characteristics:**
    -   Requires a back-end application and a database.
    -   The application takes data from the database to generate a new version of the website for each request.
    -   Allows for complex, interactive features and constantly changing content (e.g., new courses, reviews, user-specific data).
-   **Example:** A complex site like `udemy.com`.

#### 4. The Three Core Languages of the Front-End

These three technologies work together to create any website you see in a browser.

-   **HTML (Content):**
    -   Responsible for the **content and structure** of the page.
    -   Defines elements like text, images, buttons, and links.

-   **CSS (Presentation):**
    -   Responsible for the **presentation, styling, and layout** of the content.
    -   Controls colors, fonts, spacing, and element positioning.

-   **JavaScript (Interactivity):**
    -   The **programming language** of the front-end.
    -   Adds **dynamic and interactive effects** to webpages.
    -   Can be used to manipulate content (HTML) and styles (CSS), load data from servers, and build entire web applications.

**Practical Analogy: Nouns, Adjectives, and Verbs**

-   **HTML is the Noun:** It defines the thing.
    -   *Example:* `<p>` is a **paragraph**.
-   **CSS is the Adjective:** It describes the noun.
    -   *Example:* The paragraph's text is **red**.
-   **JavaScript is the Verb:** It performs an action on the noun.
    -   *Example:* **Hide** the paragraph.

---

### Summarization/Key Takeaways

-   **Client/Server Model:** The browser (**client**) requests a webpage, and the **server** responds with the necessary files (HTML, CSS, JS).
-   **Front-End:** The visible part of a website, built with HTML, CSS, and JavaScript, which is rendered by the browser.
-   **Back-End:** The invisible, server-side part of a website that often uses a database and a back-end language (like Node.js or Python) to manage data and logic.
-   **Static vs. Dynamic:**
    -   **Static:** Files are sent from the server "as is."
    -   **Dynamic:** Files are generated on the server for each request, often from a database.
-   **Core Language Roles:**
    -   **HTML:** Content & Structure (Nouns)
    -   **CSS:** Presentation & Style (Adjectives)
    -   **JavaScript:** Interactivity & Logic (Verbs)