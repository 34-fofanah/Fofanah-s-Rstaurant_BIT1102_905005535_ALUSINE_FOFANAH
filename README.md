# Fofanah's Restaurant

> **Home made food with love**

A responsive, multi-page website for **Fofanah's Restaurant**, a family restaurant in Freetown, Sierra Leone that serves authentic Sierra Leonean food made fresh every day.

This project is my submission for **Assignment 2: Development of a Responsive Multi-Page Website**. It turns my Assignment 1 Figma design into a working website using only **HTML and CSS** (no JavaScript, no frameworks).

| | |
|---|---|
| **Student** | [Alusine Fofanah] |
| **Student ID** | [905005535] |
| **Module** | [DCOMP 204 WEB DESIGN] |
| **Lecturer** | [Mr. Amadu Kamara] |


## Table of contents

1. [About the project](#about-the-project)
2. [Pages](#pages)
3. [Features](#features)
4. [Responsive design](#responsive-design)
5. [Design decisions](#design-decisions)
6. [Project structure](#project-structure)
7. [Technologies used](#technologies-used)
8. [Accessibility and best practices](#accessibility-and-best-practices)
12. [Screenshots](#screenshots)
13. [Known limitations](#known-limitations)
14. [Future improvements](#future-improvements)
16. [Author](#author)


## About the project

Fofanah's Restaurant began as a family kitchen and grew into a restaurant that people trust for honest, generous, home-cooked food. The website helps customers to:

- see what the restaurant serves and what it costs,
- order food for pickup or free delivery,
- book a table or ask about catering for an event,
- learn the story of the family and the team behind the food,
- find the address, phone number, email and opening hours quickly.

The design follows my Figma wireframes from Assignment 1. Where the wireframes did not cover something (extra menu items, FAQ, legal pages), I added content that fits the restaurant and the same visual style.



## Pages

The website has **10 pages**, all linked together through the navigation bar and footer.

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Welcome, hero banner, signature dishes, why people love us, free delivery banner |
| Menu | `menu.html` | Full menu in four categories (Rice dishes, Soups and stews, Grilled, Drinks) with prices |
| Services | `services.html` | Dine-in, takeaway, delivery and catering, plus delivery area, times and riders |
| About | `about.html` | Our story, timeline, mission, values and the team |
| Contact | `contact.html` | Address, phone, email, opening hours, booking form and map |
| Order | `order.html` | Choose dishes, pickup or delivery, and enter your details |
| Order confirmation | `confirmation.html` | Example order summary shown after submitting an order |
| FAQ | `faq.html` | Answers to common questions about orders, delivery, bookings and food |
| Terms of Service | `terms.html` | Rules for orders, delivery, payment, bookings and using the website |
| Privacy Policy | `privacy.html` | What details are collected and how they are used |



## Features

- **Consistent layout:** the same header, navigation and footer on every page.
- **Active page highlight:** the current page is highlighted in the navigation bar.
- **Mobile hamburger menu:** built with a hidden checkbox and CSS only.
- **Menu category tabs:** Rice dishes, Soups and stews, Grilled and Drinks switch with hidden radio buttons and CSS only.
- **FAQ accordion:** questions open and close using the native HTML `<details>` element.
- **Order form:** tick dishes, choose Pickup or Delivery (free), and submit to the confirmation page.
- **Booking form:** name, phone or email, date and time, number of guests and an optional message.
- **Working contact links:** `tel:` links open the phone dialler and `mailto:` links open the email app.
- **Clickable logo:** returns to the Home page from anywhere.
- **Sticky header:** the navigation stays at the top while scrolling.
- **Skip link:** "Skip to main content" for keyboard and screen reader users.
- **Images:** every image, the logo, icons and the map are real.



## Responsive design

The site uses a **mobile-first** approach. The mobile layout is the default, and the tablet and desktop layouts are added with CSS media queries.

| Device | Screen width | Layout |
|---|---|---|
| **Mobile** | under 768px | One column, hamburger menu, stacked cards and forms, full-width buttons |
| **Tablet** | 768px and up | Two-column card grids, hero text and image side by side, forms next to their content, footer in two columns |
| **Desktop** | 1024px and up | Full horizontal navigation bar, three and four column grids, four-column footer |

Other techniques used for flexible layouts:

- CSS Grid and Flexbox for all page layouts
- fluid text sizes with `clamp()`
- images that scale with `max-width: 100%` and keep their shape with `aspect-ratio`
- a flexible container that never causes sideways scrolling on small screens

I tested every page at phone, tablet and desktop widths to confirm there is no horizontal scrolling.



## Design decisions

### Colour palette

The colours are warm and appetising, which suits a restaurant.

| Role | Colour | Hex |
|---|---|---|
| Primary (buttons, headings, highlights) | Deep burgundy | `#8B1E2D` |
| Primary hover | Dark burgundy | `#6A1522` |
| Accent (underlines, borders, footer headings) | Golden amber | `#D9962B` |
| Page background | Warm cream | `#FFF8EE` |
| Soft panels and borders | Sand | `#F1E3CB` |
| Text and footer background | Charcoal brown | `#2B2118` |
| Secondary accent (confirmation message) | Olive green | `#5B6B3A` |

### Typography

- **Headings:** Georgia (serif) for a warm, traditional feel.
- **Body text:** Segoe UI, with Roboto, Helvetica and Arial as backups.
- These fonts are already installed on most devices, so nothing needs to be downloaded and the site loads quickly and works offline.

### Layout and style

- Rounded cards with soft shadows to group information clearly.
- Burgundy buttons for main actions, outlined buttons for secondary actions.
- Plenty of white space so text is easy to read on small screens.
- Prices are shown in **New Leones (Nle)**.



## Project structure


fofanahs-restaurant/
├── index.html            Home page
├── menu.html             Menu
├── services.html         Services
├── about.html            About us
├── contact.html          Contact and bookings
├── order.html            Place your order
├── confirmation.html     Order confirmation
├── faq.html              Frequently asked questions
├── terms.html            Terms of Service
├── privacy.html          Privacy Policy
├── README.md             This file
├── css/
│   └── style.css         One shared stylesheet for all pages
└── images/               Logo, placeholders and icons (SVG)


The `style.css` file is organised into numbered sections: Variables, Base, Layout, Header, Buttons, Home, Menu, Services, About, Contact, Order, Order confirmation, Footer, Tablet and Desktop. The list at the top of the file works as a table of contents.



## Technologies used

- **HTML5**: semantic page structure
- **CSS3**: custom properties (variables), Grid, Flexbox, media queries, `clamp()`
- **Git and GitHub**: version control and hosting with GitHub Pages
- **Figma**: the original design from Assignment 1

No JavaScript, no frameworks and no external libraries or fonts are used.



## Accessibility and best practices

- Semantic HTML5 elements: `header`, `nav`, `main`, `section`, `article`, `figure`, `footer`.
- One `h1` per page, with headings in a logical order.
- Every image has descriptive `alt` text .
- Every form field has a visible `<label>` linked to it.
- Clear keyboard focus outlines on links, buttons and form fields.
- "Skip to main content" link at the top of every page.
- `aria-current="page"` marks the current page in the navigation.
- Good text and background contrast.
- Image `width` and `height` attributes to avoid layout jumping while loading.
- Clean, indented code with a consistently named CSS file and clear section headings.
- Relative links and paths, so the site works from any folder or host.


| Page | Mobile | Tablet | Desktop |
|---|---|---|---|
| Home | [image] | [image] | [image] |
| Menu | [image] | [image] | [image] |
| Services | [image] | [image] | [image] |
| About | [image] | [image] | [image] |
| Contact | [image] | [image] | [image] |
| Order | [image] | [image] | [image] |

---

## Screenshot

## Home Page
<img width="1920" height="2055" alt="Home Page  - Copy" src="https://github.com/user-attachments/assets/d0dffab0-00eb-4cd4-9a47-1b1263db0048" />

## Menu Page
<img width="1920" height="1948" alt="Our Menu-Page" src="https://github.com/user-attachments/assets/17180fef-08fb-4d45-884f-ad666cabb11f" />

## Services Page
<img width="1920" height="1923" alt="Our Services-Page" src="https://github.com/user-attachments/assets/68244a92-a43b-4b1b-852f-e402b8763f17" />

## About Page
<img width="1920" height="4047" alt="About-Us-Page" src="https://github.com/user-attachments/assets/c77100e2-bcad-45aa-87be-976cfaaab938" />

## Contact Page
<img width="1920" height="2746" alt="Contact-Page" src="https://github.com/user-attachments/assets/d64e7f20-a0ae-4504-b3b1-53831a512e2a" />

## Order Page
<img width="1920" height="1848" alt="Place Your Order-Page" src="https://github.com/user-attachments/assets/5fea24cd-eb90-4e99-8e90-566dbcb823e0" />

## Confirmation Page
<img width="1920" height="1758" alt="Order confirmed Page" src="https://github.com/user-attachments/assets/9f4f8e4f-9d7e-4074-a9be-07bec34036a0" />

## FAQ Page
<img width="1920" height="2676" alt="FAQ Page" src="https://github.com/user-attachments/assets/9e88a91b-cbe3-47ad-b1a7-337c55f171dd" />

## Terms of Service Page
<img width="1920" height="2949" alt="Terms of Services Page" src="https://github.com/user-attachments/assets/30d4d349-d030-40d1-b086-6732f6a072ec" />

## Privacy Policy Page
<img width="1920" height="2571" alt="Privacy Policy Page" src="https://github.com/user-attachments/assets/a29fb0ec-d3ad-4c22-bb6d-f429e54df38a" />












## Known limitations

- **No back end:** the order form sends you to the confirmation page, but orders are not stored or sent anywhere. The confirmation page shows an example order.
- **Booking form:** it opens the visitor's email app with the message ready to send, because there is no server to receive it.
- **Order total:** the website does not calculate a total, because that would need JavaScript. The team confirms the total with the customer.
- **Placeholders:** photos, logo, map and social icons are real 
- **Social links, Terms and Privacy:** the social icons point to `#` until real profile links are added, and the Terms and Privacy pages are sample text for this assignment, not legal advice.

---

## Future improvements

- Add real photos of the food, the team and the restaurant. coz the images used here are from the internet, I just use them to make my website look real
- Connect the order and booking forms to a back end or a form service so requests are stored.
- Add JavaScript to calculate the order total automatically.
- Add an embedded interactive map.
- Add a customer reviews section.
- Add online payment options.


## Author

**[Alusine Fofanah]**
[905005535] | [BIT1102 Year2 Semester3]
[Email:fofanahalusine015@gmail.com, GitHub: 34-fofanah]

&copy; 2026 Fofanah's Restaurant. Made for educational purposes.
