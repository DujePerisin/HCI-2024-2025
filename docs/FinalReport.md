
# KUD Ante Zaninović – Final Report  
_Created and maintained by Duje Perišin_

## Table of Contents  
1. Introduction  
2. Target Audience & Design principal
3. Project Development Overview  
4. Features & Technologies  
5. Philosophy behind design
6. Application's performance  
7. Final Thoughts  

---

## 1. Introduction

The KUD “Ante Zaninović” website is the central hub for presenting who we are, what we dance, and how to get involved. The aim was to modernize the presentation of intangible Dalmatian heritage while keeping content fully editable in a CMS. Public pillars are the About, Dances and Gallery pages, with a members-only area for internal content.

Primary goals:
- Tell the group’s story clearly (leadership, styles, ensemble).
- Offer a visually rich gallery that loads fast and scales well.
- Give the user a sneak peak behind traditional culture

On load up, user is presented with a smooth and rich-looking website which offers him all the information needed to find out more about our group's activites and find the dance group i real-world, whether through e-mail, google form or actual location.

---

## 2. Target Audience & Design principal

To guide the design, I created 3 key **user personas**, based on typical envisioned visitor demographics:

### Mia – Journalist (Age 43)
(https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-1.webp)
- Needs verifiable information, short bios, awards, quality images, and a booking contact.
- Wants to get in contact ASAP with te leading people
- Needs clear navigation and visual
**UX focus:** detailed dance descriptions, credible sources, strong photography.

### Ivana – Traditional Dancer (Age 31)
(https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-2.webp)
- Focused on simplicity and readability
- Not interested in games, just clear pricing and seating info
- Needs large text, minimal interactions
**UX focus:** Dance descriptions, contact information & high-quality photos 

### Gabriela – Student (Age 22)
(https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-3.webp)
- Wants a quick sense of rehearsals and a clear path to sign up.
- Tech-savvy, is more likely to join through a website
- Looking to pass the time with people in the same age bracket
**UX focus:** modern design, google form, all info on the internet
  
These personas shaped the navigation and page structure — the site is built to be **fast, intuitive, and accessible**, even for low-tech users.

---

## 3. Project Development Overview

I first started with a general website to test out Next.js and Typescrypt and get a better feeling for the technologies by implementing:

- A fully responsive layout using **Tailwind CSS**
- Custom animations and transitions
- Mobile-first design principles

Afterwards, I got the idea to create a website for my traditional dance group so I started by planning what to include on the actual site:

- HD photos
- Story behind our dances
- Easy-to-contact information of our leading members
- Connect the traditional /w modern

When I got to the development, the only remaining problem was actual execution as I have decided to use technologies I haven't used before, but still the whole development process could be summed up in few key points:

### Key Points 
- Built reusable components in **Next.js**
- Creating a **Github** repository
- Designed a flexible **Prismic** schema for product management  
- Deploying the site on **Vercel**
- Animating components with **GSAP**
- Adding the option to sign in your Google account /w **NextAuth.js** for gmail authentication

All content, links, and posts are editable via **Prismic CMS**, allowing staff to manage updates without touching the code from any place & any device.

---
