document.addEventListener("DOMContentLoaded", function() {
    const hamburger = document.getElementById('hamburger');
    const navigation = document.getElementById('navigation');
    const closeNavBtn = document.getElementById('closeNavBtn');

    hamburger.addEventListener('click', function() {
        navigation.classList.toggle('active');
    });

    closeNavBtn.addEventListener('click', function() {
        navigation.classList.remove('active');
    });

    const miniCartTrigger = document.querySelector('.mini-cart-trigger');
    const miniCartDropdown = document.querySelector('.mini-cart-dropdown');

    miniCartTrigger.addEventListener('click', function(e) {
        e.stopPropagation();
        miniCartDropdown.classList.toggle('active');
    });

    document.body.addEventListener('click', function() {
        miniCartDropdown.classList.remove('active');
    });

    // Slider logic
    const carousel = document.querySelector('.carousel');
    const slides = document.querySelectorAll('.slide');
    const indicators = document.querySelectorAll('.indicator');
    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');

    let currentSlide = 0;

    function updateSlides() {
        carousel.style.transform = `translateX(-${currentSlide * 100}%)`;
        indicators.forEach((indicator, index) => {
            indicator.classList.toggle('active', index === currentSlide);
        });
    }

    prevBtn.addEventListener('click', function() {
        currentSlide = (currentSlide === 0) ? slides.length - 1 : currentSlide - 1;
        updateSlides();
    });

    nextBtn.addEventListener('click', function() {
        currentSlide = (currentSlide === slides.length - 1) ? 0 : currentSlide + 1;
        updateSlides();
    });

    indicators.forEach((indicator, index) => {
        indicator.addEventListener('click', function() {
            currentSlide = index;
            updateSlides();
        });
    });

    // Initialize slides
    updateSlides();
});

document.addEventListener("DOMContentLoaded", function() {
    const cartIcon = document.querySelector('.cart-icon');
    const cartDropdown = document.querySelector('.cart-dropdown');

    cartIcon.addEventListener('click', function(e) {
        e.stopPropagation();
        cartDropdown.classList.toggle('active');
    });

    document.body.addEventListener('click', function() {
        cartDropdown.classList.remove('active');
    });

    // Slider logic
    const carousel = document.querySelector('.carousel');
    const slides = document.querySelectorAll('.slide');
    const indicators = document.querySelectorAll('.indicator');
    const prevBtn = document.getElementById('prevBtn');
    const nextBtn = document.getElementById('nextBtn');

    let currentSlide = 0;

    function updateSlides() {
        carousel.style.transform = `translateX(-${currentSlide * 100}%)`;
        indicators.forEach((indicator, index) => {
            indicator.classList.toggle('active', index === currentSlide);
        });
    }

    prevBtn.addEventListener('click', function() {
        currentSlide = (currentSlide === 0) ? slides.length - 1 : currentSlide - 1;
        updateSlides();
    });

    nextBtn.addEventListener('click', function() {
        currentSlide = (currentSlide === slides.length - 1) ? 0 : currentSlide + 1;
        updateSlides();
    });

    indicators.forEach((indicator, index) => {
        indicator.addEventListener('click', function() {
            currentSlide = index;
            updateSlides();
        });
    });

    // Initialize slides
    updateSlides();
});

document.getElementById('nav-toggle').addEventListener('click', function() {
    document.getElementById('nav-list').classList.toggle('active');
});

document.getElementById('nav-close').addEventListener('click', function() {
    document.getElementById('nav-list').classList.remove('active');
});

document.addEventListener("DOMContentLoaded", function() {
    const categoryToggle = document.getElementById('categoryToggle');
    const categoriesList = document.getElementById('categoriesList');

    categoryToggle.addEventListener('click', function() {
        categoriesList.classList.toggle('active');
    });
});
