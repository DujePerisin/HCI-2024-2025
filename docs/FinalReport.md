
# KUD Ante Zaninović – Final Report  
_Created and maintained by Duje Perišin_

## Table of Contents  
1. Introduction  
2. Target Audience & Design principal
3. Project Development Overview  
4. Core Features 
5. Philosophy behind design
6. CMS overview
7. Application's performance  
8. Final Thoughts  

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
![Mia - Journalist](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-1.webp)
- Needs verifiable information, short bios, awards, quality images, and a booking contact.
- Wants to get in contact ASAP with te leading people
- Needs clear navigation and visual
**UX focus:** detailed dance descriptions, credible sources, strong photography.

### Ivana – Traditional Dancer (Age 31)
![Ivana - Traditional Dancer](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-2.webp)
- Focused on simplicity and readability
- Not interested in games, just clear pricing and seating info
- Needs large text, minimal interactions
**UX focus:** Dance descriptions, contact information & high-quality photos 

### Gabriela – Student (Age 22)
![Gabriela - Student](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/target-audience-3.webp)
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

## 4. Core Features

- About: hero with poster/video, group story & styles, dance history.
- Gallery: intro + PhotoShowcase; shows items in batches of 3 with a Load more control; optional filtering by category/style and light emphasis on the first three photos.
- CMS-driven navigation: links configurable in Prismic.
- CMS-optimised MetaData: all the Metadata can also be configured through CMS to ease the future development
- Members area: Google sign-in (NextAuth), foundation for private materials and notices.
- SEO: meta title/description/image pulled from Prismic via generateMetadata and further optimised in code.
- Sign up form: google sing-up form available for potential new members
- Back-to-top: at any time, user can decide to go back to top by clicking any KUD Ante Zaninović logo
- Footer info: footer contains detailed list of the most information presented on the site
- Terms & Conditions: user can view our online policy if he/she has any confusion with handling our material
- Social media: all our link can be found on the site along with the location of our headquarters

## 5. Philosophy behind design

To support intuitive and accessible user experience, the interface was designed with the **CRAP design principles** in mind:

#### Contrast
- Smooth, rich and dark texture is applied throughout the site to give the user the feeling of richness of traditional culture
- All the design elements (including transitions and placements) were created with that in mind so they are darker with white accent which stick out

#### Repetition
- Consistent styling of components such as built-in components with smooth transitions helps users recognize recurring patterns and navigate with ease.
- Sidebar and navbar help the user not get lost while spacing, font sizes, and section layouts follow a consistent rhythm to reinforce familiarity

#### Alignment
- All UI elements are neatly aligned using Tailwind’s grid and flexbox utilities, providing a clean and professional layout.
- Text, icons, and buttons are aligned to guide the eye smoothly through each section without confusion.
- 
#### Proximity
- Related content (e.g., dance name + description + next button) is grouped closely to indicate association.
- Adequate spacing is used to separate unrelated content blocks, reducing clutter and improving scan-ability.

### Other design thoughs

#### Accessibility
- All the alt tags were applied to help those with bad connection or either those less fortunate
- Development process always included that part

#### Memory
- During the better part of group's 25 year history, a lot of memories were made
- Website includes loads of HD photos for members to freely use


> By applying these principles throughout the site, the interface becomes both functional and aesthetically pleasing — reinforcing trust and usability for every visitor, whether they’re a tech-savvy student or a retired tourist.


---

## 6. CMS overview
Prismic CMS was used in this project and from the following photos you can see few example of the CMS side of the development process, which can be summed up in few lines:
1. Creating a new page
2. Adding neccessary "slices", which are basically components for which Prismic helps generate Metadata and attributed
3. Populating slices & pages with relevant data

![creating-page](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/cms-overview-1.PNG)
![adding-slices](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/cms-overview-2.PNG)
![populating-w-data](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/cms-overview-3.PNG)

---

## 7. Application's performance

The site is hosted on **Vercel**, with the official domain [kud-ante-zaninovic.vercel.app](https://kud-ante-zaninovic.vercel.app/)

### Deployment details:
- Production URL: [kud-ante-zaninovic.vercel.app](https://kud-ante-zaninovic.vercel.app/)
- CMS studio is connected to Prismic CMS for real-time content editing
- It utilizes a Content Delivery Network (CDN) that leverages edge caching, 

### 📊 Performance

#### Current practices
- SSR/SSG data fetches from Prismic; minimal client-side code (state only for filter and pagination).
- Images: imgixParams={{ auto: 'format,compress', q: 60 }}, sizes, and priority for the first visible item; lazy-loading for the rest.
- Batch rendering: gallery in groups of 3 → fewer network requests and improved Total Blocking Time.
- Type safety & guards: isFilled checks and generated types reduce hydration issues.

#### Potential enhancements
- Add preconnect to images.prismic.io and the repo CDN.
- Use Vercel Analytics / Speed Insights for ongoing monitoring.
- Gallery lightbox with prefetching of the next image in the batch.
- ISR revalidation for frequently updated sections (e.g., announcements).

![Desktop performance](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/performance-desktop.PNG)

![Mobile performance](https://github.com/DujePerisin/HCI-2024-2025/blob/main/assets/performance-mobile.PNG)
---

## 8. Final Thoughts

Throught development I was concerned how far I can push this project, but now that I'm writting this I can say that even though there is still plenty to add, I am proud of where it is currently. Through this website, our rich traditonal folk culture will be perserved in a modern format.

From the stage to the website, the goal is the same: keep traditional steps alive today, with care, clarity, and pride.


