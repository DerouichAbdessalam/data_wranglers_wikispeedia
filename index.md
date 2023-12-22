---
layout: page
title: "NAVIGATING THE MAZE OF THE MIND"
background: '/img/brain.png'
---
**Intro: The Enigmatic World of Wikispeedia**

Our minds are complex instruments, constantly composing thoughts, yet we know so little about the notes behind the music. Usually discreet, our brains occasionally let the curtain slip, revealing their inner workings in unexpected settings. 
Enter Wikispeedia: a cognitive revelation hidden in a simple game. Players dart from one Wikipedia article to the next, aiming for a target. As they navigate, they leave behind a trail of thoughts. What secrets do these trails unravel about the voyagers? 
Dive in and with us as ew explore these mental pathways.

---
**Part 1: Game Characteristics - Decoding Wikispeedia**

Before 

To crack the code of player behavior, we first need to delve into the game's essence. In our game players journey through a maze of Wikipedia articles, connecting the dots in a race to the finish. 

//in here we give game detail and statistics about paths, categories and so on 


---
**Part 2: Let’s talk strategy**

Now, let’s talk strategy. We have an expansive universe of paths, categories, and articles, what I step go to strategy in our game, to uncover this we start by ranking articles based on their popularity. 
Players often head for the peaks since they offer a better view (navigational options). But that's  just scratching the surface.





Mapping the Mental Terrain:

What happens when we intertwine these paths with the categories of the articles? We uncover something more profound than the apparent links between categories statically present in wikspeedia articles. It's about the choices players make. Do we focus on their completed journeys or the ones they abandon? By mapping out how often categories appear together, we find that both victorious and failed attempts share similar patterns. 

… introduce mind maps 

---

**Part 3: Extracting the Insights**

Now that we know where to look and what to look for : – the aggregate paths and proximity metrics – we conjure up a mind map of the major cognitive connections. 

Even more fascinating, by isolating the paths of veteran players, we see a clear evolution from their early attempts to their later, more refined strategies. What emerges is a collective portrait of cognitive growth.

---
**Part 4: The Odyssey of an Exceptional Player**

But there's an outlier in our adventure: a player who's navigated through about 5000 games. What’s the story behind this marathon of the mind? This player is like a rare gem in our exploration, offering a unique perspective into the intricate workings of a seasoned Wikispeedia navigator. Let’s dive into this exceptional journey and see what secrets we can uncover.


---

**Plots**


<!-- pyramids plot -->

<input type="range" min="4" max="25" value="4" id="pathLengthSlider" onchange="updatePlot(this.value)">
<p>Path Length: <span id="pathLengthValue">4</span></p>
<div id="plotContainer">
    <iframe id="plotFrame" src="html_plots/interactive_pyramids/plot_path_length_4.html" width="100%" height="600" frameborder="0"></iframe>
</div>

<script>
function updatePlot(value) {
    var basePlotUrl = document.getElementById("basePlotUrl").getAttribute("data-url");
    document.getElementById("pathLengthValue").innerText = value;
    document.getElementById("plotFrame").src = "html_plots/interactive_pyramids/plot_path_length_" + value + '.html';
}
</script>



<!-- ========================= -->



<!-- degree frequency plot -->

<iframe src="html_plots/Incoming_plot.html" width="100%" height="600"></iframe>


<iframe src="html_plots/Outgoing_plot.html" width="100%" height="600"></iframe>


<!-- ========================= -->

<!-- category frequency plot -->

<iframe src="html_plots/category_frequency.html" width="100%" height="600"></iframe>

<!-- ========================= -->
<!-- hmap plots plot -->
<iframe src="html_plots/heat_maps/hmap_up_finished.html" width="100%" height="600"></iframe>


<iframe src="html_plots/heat_maps/hmap_down_finished.html" width="100%" height="600"></iframe>

<iframe src="html_plots/heat_maps/hmap_up_unfinished.html" width="100%" height="600"></iframe>

<iframe src="html_plots/heat_maps/hmap_down_unfinished.html" width="100%" height="600"></iframe>

<!-- ========================= -->



<!-- HTML for Dropdown Menu -->
<select id="categorySelect" onchange="updateImage()">
    <option value="category1">Category 1</option>
    <option value="category2">Category 2</option>
    <option value="category3">Category 3</option>
    <!-- Add more categories as needed -->
</select>

<!-- Image Placeholder -->
<img id="categoryImage" src="html_plots/brain_categories_images/category1.png" alt="Category Image"/>

<!-- JavaScript to Update Image -->
<script>
function updateImage() {
    var selectedCategory = document.getElementById('categorySelect').value;
    var imagePath = 'html_plots/brain_categories_images/' + selectedCategory + '.png';
    document.getElementById('categoryImage').src = imagePath;
}
</script>

<!-- CSS for Styling -->
<style>

.dropdown-container {
    display: flex;
    justify-content: center; /* Center horizontally */
    align-items: center; /* Center vertically */
    height: 100vh; /* Full height of the viewport */
    font-family: 'serial'; /* Apply a font similar to the one in the image */
}

#categorySelect {
    padding: 10px;
    border: 2px solid #007bff;
    border-radius: 5px;
    background-color: white;
    font-size: 16px;
    color: #007bff;
    cursor: pointer;
}


#categoryImage {
    width: 100%;
    max-width: 700px; /* Adjust as needed */
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    margin-top: 20px;
}

</style>


