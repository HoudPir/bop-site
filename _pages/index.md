---
title: Home
permalink: "/"
layout: default
custom_css: index.css
---

<div class="top-buttons">
    <a href="#" class="btn">🌐 Internet Banking</a>
    <a href="#" class="btn">🏷️ Discounts & Offers</a>
    <a href="#" class="btn">📍 Branch / ATM Locator</a>
  </div>

  <div class="slideshow-container" id="slideshow" onmouseenter="pauseSlideshow()" onmouseleave="resumeSlideshow()">
    <button class="prev" onclick="prevSlide()">❮</button>
    <button class="next" onclick="nextSlide()">❯</button>
  </div>

  <div class="slideshow-indicators" id="slideIndicators"></div>

  <section class="quick-links">
    <a href="#">Roshan Digital</a>
    <a href="#">Raast</a>
    <a href="#">Islamic Banking</a>
    <a href="#">Complaints</a>
    <a href="#">Investor Info</a>
    <a href="#">SME Portal</a>
  </section>

  <footer>
    UAN: 111 – 267 – 200 | Grievance Commissioner Cell for Overseas Pakistanis | © 2025 The Bank of Punjab
  </footer>

  <script>
    function toggleTheme() {
      const current = document.documentElement.getAttribute('data-theme');
      const next = current === 'dark' ? 'light' : 'dark';
      document.documentElement.setAttribute('data-theme', next);
    }

    // Slideshow logic
    const imageUrls = [
      "https://www.bop.com.pk/images/posters/Apple%20Campaign.jpg",
      "https://www.bop.com.pk/images/posters/EidulAzha.jpg",
      "https://www.bop.com.pk/images/posters/Raast.jpg"
    ];

    const slideshow = document.getElementById("slideshow");
    const indicators = document.getElementById("slideIndicators");
    let currentSlide = 0;
    let slideInterval;

    imageUrls.forEach((url, index) => {
      const slide = document.createElement("div");
      slide.className = "slide";
      if (index === 0) slide.classList.add("active");
      slide.innerHTML = `<img src="${url}" alt="Slide ${index + 1}" />`;
      slideshow.insertBefore(slide, slideshow.querySelector(".prev"));

      const dot = document.createElement("button");
      dot.addEventListener("click", () => {
        currentSlide = index;
        showSlide(currentSlide);
        resetIndicators();
      });
      indicators.appendChild(dot);
    });

    const slides = document.querySelectorAll(".slide");
    const indicatorDots = indicators.querySelectorAll("button");

    function showSlide(index) {
      slides.forEach(slide => slide.classList.remove("active"));
      slides[index].classList.add("active");
      resetIndicators();
    }

    function resetIndicators() {
      indicatorDots.forEach(dot => dot.classList.remove("active"));
      indicatorDots[currentSlide].classList.add("active");
    }

    function nextSlide() {
      currentSlide = (currentSlide + 1) % slides.length;
      showSlide(currentSlide);
    }

    function prevSlide() {
      currentSlide = (currentSlide - 1 + slides.length) % slides.length;
      showSlide(currentSlide);
    }

    function pauseSlideshow() {
      clearInterval(slideInterval);
    }

    function resumeSlideshow() {
      slideInterval = setInterval(nextSlide, 3000);
    }

    resumeSlideshow();
    resetIndicators();
  </script>