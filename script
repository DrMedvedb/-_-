document.addEventListener("DOMContentLoaded", () => {
    // --- 1. Горизонтальная прокрутка меню колесиком мыши ---
    const menuCarousel = document.getElementById("menuCarousel");
    if (menuCarousel) {
        menuCarousel.addEventListener("wheel", (evt) => {
            evt.preventDefault(); 
            menuCarousel.scrollLeft += evt.deltaY; 
        });
    }

    // --- 2. Логика для модального окна (Lightbox) ---
    const lightbox = document.getElementById("lightbox");
    const lightboxImg = document.getElementById("lightbox-img");
    const closeBtn = document.querySelector(".close-btn");
    const images = document.querySelectorAll(".lightbox-trigger");

    images.forEach(img => {
        img.addEventListener("click", () => {
            lightbox.style.display = "flex";
            lightboxImg.src = img.src; 
        });
    });

    closeBtn.addEventListener("click", () => {
        lightbox.style.display = "none";
    });

    lightbox.addEventListener("click", (e) => {
        if (e.target === lightbox) {
            lightbox.style.display = "none";
        }
    });

    document.addEventListener("keydown", (e) => {
        if (e.key === "Escape" && lightbox.style.display === "flex") {
            lightbox.style.display = "none";
        }
    });
});
