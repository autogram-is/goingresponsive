---
title: GLOSSARY
tocOrder: 11
---
Responsive web design introduces a new way of talking about web design and development. I present my personal—often biased—definitions for your reference. Don’t toss these words around assuming that everyone knows what you mean. Discuss this glossary with your team to build a shared understanding of how responsive design is different.

**adaptive** — While responsive designs fluidly serve all devices with one set of client-side code, adaptive solutions require server-side negotiation to serve different content or HTML to the same URL, targeted based on device type or other known contextual variables. See **adaptive content**, **adaptive** **design**.

**adaptive content** — Structured content that can be targeted based on known characteristics of the user or the device. Serving different content to smartphones, tablets, and desktops is one common use, but adaptive content also supports contextual targeting (like location or time of day) and user-specific personalization.

**adaptive design** — Serving different HTML to solve device-specific layout problems. This can include device-specific pages (like a mobile landing page) or even device-specific functionality (like serving a different table to smartphone and desktop users).

**adaptive grid** — A series of fixed-width grid structures that snap into place at device-specific sizes, rather than being completely fluid, as in a fully responsive design. Unlike other adaptive solutions, adaptive grids do not require different HTML or server-side negotiation. See **fixed-width**, **fluid** **grid**.

**breakpoint** — The specified browser widths and heights where the layout shifts to rearrange, collapse, or hide elements on the page in a responsive design. Major breakpoints define significant changes in the design (like shifting the layout from a single column to two columns.) Minor breakpoints define small adjustments to improve readability or usability (like increasing the font size or adding more padding around elements.)

**canonical URL** — When the same web page may appear at multiple URLs, Google prefers that a single URL is selected as the preferred URL for indexing. To prevent Google from indexing the identical content on both a desktop site and an m-dot domain, a canonical URL defines which version should be used. See **m-dot**.

**content choreography** — Maintaining correct hierarchy of modules as layouts shift across multiple columns. Rather than simply stacking modules (so items in the right column at larger breakpoints wind up at the bottom of the page at smaller breakpoints), these modules can be interleaved at smaller breakpoints so they appear in the correct order.

**design system** — A defined set of grids, color palettes, type treatments, and graphic elements like lines, buttons, and image styles, which can be applied in different ways to create a more consistent visual identity. See **pattern library**, **front-end** **framework**.

**designing in the browser** — Using code-based prototyping tools in the design process instead of applications like Photoshop that provide static layouts. Front-end frameworks are often used to simplify this process.

**device detection** — Using a third-party library (often proprietary) to identify the device type and capabilities of the device. Device detection is required for adaptive and m-dot sites; responsive sites are built fluidly on the client side and do not require it. See **adaptive**, **m-dot**, **UA** **detection**.

**fixed-width** — A web page with a static, predefined pixel width that does not change in relation to the size of the browser window. Before responsive design, most websites had a fixed width of around 1000 pixels, which was designed to fill the screen of a 1024×768 monitor, the most common screen resolution at the time. See **adaptive grid**, **fluid** **grid**.

**fluid grid** — Responsive design is based on a fluid grid, where the maximum width of the web page, as well as the columns and containers within, are defined using proportional widths instead of fixed pixel-based dimensions. Objects change their widths and heights in relation to the size of the browser window. See **adaptive grid**, **fixed-width**, **relative** **units**.

**the fold** — Content placed at the top of the page that does not require scrolling to view is considered “above the fold.” Because mobile devices have diverse, smaller screen sizes, it is less important to place information above the fold. Design techniques should encourage scrolling and ensure that calls to action are placed where users are prepared to act on them.

**front-end** **framework** — A mostly complete package of all the commonly used structures, layouts, and components that make up a website, implemented with standardized HTML, CSS, and JavaScript so developers can reuse predefined (but generic) code. See **design system**, **pattern** **library**.

**graceful** **degradation** — Delivers an ideal experience to users with modern browsers or devices, but offers fallbacks for situations where the ideal experience is not supported. See **progressive** **enhancement**.

**hamburger menu** — An icon showing three lines, which users tap to see the navigation options on devices with insufficient screen real estate to display the full navigation bar. Critics argue that hiding the menu under an unclear icon makes the site more difficult to navigate.

**high-res images** — Devices with higher pixel density (like Retina devices from Apple) require images with the same pixel density—otherwise the images appear pixellated or too small. Images with higher resolution are heavier and will slow down performance, so they should only be sent to devices that require them. See **responsive** **images**.

**m-dot** — Instead of a single responsively designed website, a separate website served only to mobile devices, usually served on a subdomain like m.domain.com. See **device** **detection**.

**media queries** — Enable the browser to test whether a device supports a particular media type and desired features, like a screen that has a minimum width of 780 pixels. In response, the browser loads different CSS which changes the way the content appears. Adding support for media queries to the CSS3 spec is what made responsive web design possible.

**mobile first** — Using the constraints and capabilities of mobile devices to focus and prioritize. By starting with the most constrained smartphone form factor, teams are forced to make choices. It’s easier to start small and work up than to start with a desktop site and try to fit everything into a smaller view.

**pattern library** — A set of reusable interactive elements, like date pickers, pagination, or navigation styles, that developers can copy and paste into designs to save time and foster consistency across the site. Usually custom-designed for a specific website or brand and intended to be used as independent objects. See **design system**, **front****\-end** **framework**.

**perceived performance** — Techniques to optimize how fast the website appears to load so users can begin interacting. Sites that enable users to begin interacting more quickly feel faster, even if the page has not fully rendered.

**pixel perfect** — Coding and testing websites so they are identical across every browser. A responsive design does not need to look the same in all browsers.

**progressive disclosure** — A design technique that sequences the flow of information across screens, so users can focus on what’s required to complete a task without being distracted or overwhelmed by unnecessary information. It is not the same as progressive enhancement.

**progressive enhancement** — Delivers a baseline of usable functionality to everyone, then layers on additional features or enhancements for browsers that can support them. By starting with the lowest common denominator and testing for support for enhancements before applying them, more capable browsers can deliver a better user experience while less capable browsers still deliver a functional experience. See **graceful** **degradation**.

**prototype** — Responsive designs require a prototype for making design decisions, rather than relying solely on static comps. Responsive prototypes often show only front-end behaviors, though some are integrated with data from the backend.

**relative** **units** — Responsive designs use proportional sizing, like percentages for widths or ems for font sizes, rather than using absolute units like pixels. Sizes of page elements like fonts or images are defined in relation to the size of the browser window.

**responsive images** — Because screens have different sizes and pixel densities, different images often need to be sent to different devices. New HTML markup attributes `srcset`, `sizes`, and `picture` enable developers to scale image sizes appropriately and provide multiple image source files.

**user agent (UA) detection** — Identifying the browser rendering engine using the user-agent string for the purpose of serving different HTML to different browsers. Notoriously inaccurate, as browsers identify themselves as other browsers to “spoof” UA detection. Responsive design does not require UA detection. See **device** **detection**.

**viewport** — The size of a webpage rendered in the browser window minus any browser chrome. Early mobile devices relied on two sizes of viewports: the visual viewport defined the visible screen real estate (say, 320 pixels), while the layout viewport was a larger virtual screen size (say, 980 pixels). This enabled existing desktop websites to be scaled and zoomed on smaller devices.

**web standards** — A philosophy of web design and development that encourages adhering to formal standards and practices for writing HTML, CSS, and JavaScript, to ensure accessibility and valid semantic encoding.
