# BioDestino Website

## Description

BioDestino is a company specialized in the collection, transportation, treatment, and proper disposal of biological waste. This project showcases the design and development of a modern institutional website created to present the company's mission, services, clients, and operational workflow.

The website was designed as a single-page experience, providing intuitive navigation and interactive elements that guide users through every stage of BioDestino's service process, from the initial contact to final certification.

---

## Live Website

🔗 Add the website URL here

---

## Features

* Institutional presentation of BioDestino;
* Single-page website structure;
* Interactive navigation between sections;
* Service presentation and explanation;
* Client showcase section;
* Operational workflow presentation;
* Animated information carousel;
* Animated icons and visual elements;
* Smooth scrolling navigation;
* Outlook integration for contact requests;
* Direct phone call functionality on supported devices;
* Modern and user-friendly interface.

---

## Technologies Used

* Figma
* UI/UX Design
* Interactive Prototyping
* HTML5
* CSS3
* JavaScript

---
### Home Section

[Look at the Home Section](https://drive.google.com/file/d/1MNfYsn6lYn-fwOOPR3F9eaxmrnRj54p3/view?usp=drive_link)
### Clients Section

![Look at the Clients Section](https://drive.google.com/file/d/1BR74oICQBtZ5xG5IX0f2LrF8KCG-WyLJ/view?usp=drive_link)

## Interactive Features

### Service Workflow

🎥 [Watch the Workflow Animation](https://drive.google.com/file/d/1oCtEZM7dkocFPi-pisIoUxBc5N6fxDpw/view?usp=drive_link)

### Carousel Animation

🎥 [Watch the Carousel Animation](https://drive.google.com/file/d/1P-QPCVn7_s7n73AN00vWUsyb-a5d0G7B/view?usp=drive_link)

### Header Navigation

🎥 [Watch the Header Navigation Animation](https://drive.google.com/file/d/1YUKmF5RwvY3gx1sDHbNVxQglbijK7q8F/view?usp=drive_link)


### Services

🎥 [Watch the Services Navigation](https://drive.google.com/file/d/13eMbamMY_QguTDeCMh6Klqm07XANuo64/view?usp=drive_link)

### "Conheça Nossos Serviços" Botton

🎥 [Watch the "Conheça Nossos Serviços" botton funcionality](https://drive.google.com/file/d/1ed8qOAAJPjjoSNGg3G74gLVFUvk_-kEf/view?usp=drive_link)

---

## Code Highlights

### Smooth Navigation Between Sections

This functionality allows users to navigate seamlessly throughout the website.

```javascript
const scrollToSection = (id: string) => {
    const element = document.getElementById(id);
    if (element) {
      setIsMenuOpen(false);
      setIsContactOpen(false);
      setTimeout(() => {
        element.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }, 100);
    }
  };
```

### Automatic Carousel

The carousel automatically rotates featured content, creating a dynamic user experience.

```javascript --> O mecanismo central — scroll vertical → movimento horizontal
export function HorizontalScroll() {
  const targetRef = useRef(null);
  const { scrollYProgress } = useScroll({
    target: targetRef,
    offset: ['start start', 'end end']
  });

  const x = useTransform(scrollYProgress, [0, 1], ['0%', '-75%']);
```
```javascript --> O "truque" do sticky
 <section ref={targetRef} style={{ position: 'relative' }} className="hidden md:block h-[400vh] bg-gradient-to-br from-gray-900 to-gray-800">
        <div className="sticky top-0 h-screen flex items-center overflow-hidden">
          <div className="absolute inset-0 bg-gradient-to-r from-[#2D6A2E]/20 to-[#5C4033]/20"></div>

          <motion.div
```

### Animated Workflow Timeline

Visual animations help users understand the operational process in a clear and engaging way.

```javascript --> Parallax Section
export function Process() {
  const containerRef = useRef(null);
  const { scrollYProgress } = useScroll({
    target: containerRef,
    offset: ['start end', 'end start']
  });

  const backgroundY = useTransform(scrollYProgress, [0, 1], ['0%', '20%']);
```

```HTML --> The Line
<div className="absolute left-1/2 top-0 bottom-0 w-1 bg-gray-200 -translate-x-1/2">
  <motion.div
    style={{ height: lineHeight }}
    className="... origin-top"
  />
</div>
```

---

## What I Learned

Throughout the development of this project, I strengthened my skills in:

* UI/UX Design;
* Information Architecture;
* Corporate Website Design;
* Interactive Navigation Design;
* Animation Planning and Implementation;
* User Experience Optimization;
* Responsive Design Principles;
* Professional Prototyping with Figma;
* Front-End Development using HTML, CSS, and JavaScript.

---

## Author

**Gustavo Pinheiro Gaspar Cordeiro**

Developer and Designer responsible for the conception, design, prototyping, and development of the BioDestino website.
