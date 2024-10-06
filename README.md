# Horizontal Scroll Image Gallery
<p>The **Horizontal Scroll Image Gallery** is an interactive, modern gallery designed to showcase images in a horizontal scrolling format. Using HTML, CSS, and JavaScript, this gallery allows users to navigate through a collection of images either by clicking navigation buttons or using the mouse wheel to scroll.</p>
<h2>Key Features</h2>
<h3>Image Display</h3>
<p>Images are arranged in a grid format within a horizontally scrollable container. Users can view six images at a time, presented in two rows. The images are styled with a grayscale effect, which changes to full color when hovered over, adding a dynamic and interactive feel.</p>
<h3>Navigation</h3>
<h4>Scroll Navigation</h4>
<p>Users can scroll through the gallery horizontally using their mouse wheel, making it easy to browse through the images smoothly without disrupting the layout.</p>
<h4>Button Navigation</h4>
<p>The gallery includes **Back** and **Next** buttons on either side, which allow users to move through the images in smooth, predefined increments.</p>
<h3>Visual Design</h3>
<p>The gallery features a minimalist design with a dark background that emphasizes the images. The gallery container is centered on the page, and the images are displayed in a grid, maintaining symmetry and visual appeal.</p>
<h4>Hover Effect</h4>
<p>The hover effect on the images changes them from grayscale to color and slightly enlarges them, drawing attention to the individual images as users interact with the gallery.</p>
<h3>Responsive Design</h3>
<p>The layout is designed to be fully responsive, allowing users to enjoy the gallery on different devices and screen sizes without losing the intended aesthetic or functionality.</p>
<h2>Technical Overview</h2>
<h3>HTML Structure</h3>
<p>The HTML structure includes a wrapping container for the entire gallery, navigation buttons, and the images, which are arranged within grid-like `div` containers.</p>
<h3>CSS Styling</h3>
<p>CSS is used to style the layout, images, and navigation buttons. The gallery is styled with flexbox to enable horizontal scrolling, while the individual images are placed within a grid layout. The design includes smooth transitions for scrolling and image hover effects.</p>
<h4>Transitions and Hover Effects</h4>
<p>CSS transitions are used to control the hover effects, enabling the grayscale-to-color transition and slight enlargement of images when hovered over.</p>
<h3>JavaScript Functionality</h3>
<p>JavaScript is used to handle the scroll behavior and button functionality. Event listeners are added to the gallery container for mouse wheel scrolling, as well as to the **Back** and **Next** buttons for smooth navigation through the image sets.</p>

    let scrollContainer = document.querySelector(".gallery");
    let backBtn = document.getElementById("backBtn");
    let nextBtn = document.getElementById("nextBtn");
    
    scrollContainer.addEventListener("wheel", (evt) => {
        evt.preventDefault();
        scrollContainer.scrollLeft += evt.deltaY;
        scrollContainer.style.scrollBehavior = "auto";
    });
    
    nextBtn.addEventListener("click", () => {
        scrollContainer.style.scrollBehavior = "smooth";
        scrollContainer.scrollLeft += 900;
    });
    
    backBtn.addEventListener("click", () => {
        scrollContainer.style.scrollBehavior = "smooth";
        scrollContainer.scrollLeft -= 900;
    });

<h2>Conclusion</h2>
<p>The **Horizontal Scroll Image Gallery** is a sleek and intuitive image gallery with a horizontal scroll feature. With smooth transitions, hover effects, and responsive design, it provides an engaging and visually appealing way to showcase images, suitable for modern websites and portfolios.</p>
