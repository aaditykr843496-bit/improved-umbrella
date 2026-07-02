// your code goes here
/* ==========================================
   PORTFOLIO WEBSITE - script.js
========================================== */

// ===== Smooth scrolling for navigation =====
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener("click", function (e) {
        e.preventDefault();

        const target = document.querySelector(this.getAttribute("href"));

        if (target) {
            target.scrollIntoView({
                behavior: "smooth",
                block: "start"
            });
        }
    });
});


// ===== Custom Glow Cursor =====
const cursor = document.querySelector(".cursor");

document.addEventListener("mousemove", (e) => {

    if (cursor) {

        cursor.style.left = e.clientX + "px";
        cursor.style.top = e.clientY + "px";

    }

});


// ===== Navbar Background on Scroll =====
const nav = document.querySelector("nav");

window.addEventListener("scroll", () => {

    if (window.scrollY > 50) {

        nav.style.background = "rgba(5,15,35,.80)";
        nav.style.backdropFilter = "blur(30px)";
        nav.style.boxShadow = "0 20px 40px rgba(0,0,0,.45)";

    } else {

        nav.style.background = "rgba(255,255,255,.05)";
        nav.style.backdropFilter = "blur(20px)";
        nav.style.boxShadow = "0 15px 40px rgba(0,0,0,.35)";

    }

});


// ===== Fade In Animation =====
const observer = new IntersectionObserver((entries) => {

    entries.forEach(entry => {

        if (entry.isIntersecting) {

            entry.target.classList.add("show");

        }

    });

}, {
    threshold: 0.15
});

document.querySelectorAll(".section").forEach(section => {

    section.classList.add("hidden");

    observer.observe(section);

});


// ===== Button Ripple Effect =====
document.querySelectorAll(".btn").forEach(btn => {

    btn.addEventListener("click", function (e) {

        const ripple = document.createElement("span");

        const x = e.offsetX;
        const y = e.offsetY;

        ripple.style.left = x + "px";
        ripple.style.top = y + "px";

        ripple.className = "ripple";

        this.appendChild(ripple);

        setTimeout(() => {

            ripple.remove();

        }, 600);

    });

});


// ===== Floating Hero =====
const hero = document.querySelector(".hero-content");

window.addEventListener("mousemove", (e) => {

    if (!hero) return;

    const x = (window.innerWidth / 2 - e.pageX) / 40;
    const y = (window.innerHeight / 2 - e.pageY) / 40;

    hero.style.transform =
        `translate(${x}px, ${y}px)`;

});


// ===== Random Background Glow =====
const bg = document.querySelector(".bg-animation");

setInterval(() => {

    if (!bg) return;

    const x = Math.random() * 100;
    const y = Math.random() * 100;

    bg.style.background =
        `
radial-gradient(circle at ${x}% ${y}%,
rgba(0,160,255,.35),
transparent 25%),

radial-gradient(circle at top,
#0b7cff 0%,
transparent 35%),

radial-gradient(circle at bottom,
#003cff 0%,
transparent 35%),

#01030b
`;

}, 5000);


// ===== Console Welcome =====
console.log(
"%cWelcome to Aadity Kumar Portfolio",
"color:#00aaff;font-size:20px;font-weight:bold;"
);

console.log(
"%cDesigned with HTML, CSS & JavaScript",
"color:white;font-size:14px;"
);
