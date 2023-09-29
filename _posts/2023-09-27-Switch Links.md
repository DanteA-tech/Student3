
<html>
<head>
    <title>Button Link Example</title>
</head>
<body>
    <a href="https://www.ulta.com/p/luna-rossa-black-eau-de-parfum-xlsImpprod18731053" id="link1" class="button" target="_blank">Ingredients</a>
    <a href="https://www.fragrantica.com/perfume/Prada/Luna-Rossa-Black-48682.html" id="link2">prada black scent profile</a>
    <button id="toggleButton" onclick="switchLinks()">Switch Links</button>
    <p>Switch Count: <span id="switchCount">0</span></p>
    <p>Link 1: <span id="link1Text">https://www.ulta.com/p/luna-rossa-black-eau-de-parfum-xlsImpprod18731053</span></p>
    <p>Link 2: <span id="link2Text">https://www.fragrantica.com/perfume/Prada/Luna-Rossa-Black-48682.html</span></p>
</body>
</html>
<div>
    <!-- notice how tags can be put INSIDE each other -->
    <p>Prada introduced Prada Luna Rossa Black to expand its Luna Rossa line, catering to consumers seeking a bold and distinctive fragrance experience. This fragrance is a captivating addition, blending aromatic notes of bergamot and angelica with intense patchouli, creating a unique and sensual scent profile. Prada aimed to offer a sophisticated and mysterious olfactory journey for those who appreciate the brand's commitment to innovation and luxury.
    </p>
    <p>
        <!-- Your image here -->
    </p>
    <p>Prada Luna Rossa Black is a versatile fragrance suitable for various occasions, making it perfect for both daytime and evening wear. Its intriguing blend of notes, including bergamot and patchouli, strikes a balance between elegance and intensity, making it a great choice for formal events, romantic evenings, or even everyday use.
    </p>
</div>

<script>
    var link1 = document.getElementById("link1");
    var link2 = document.getElementById("link2");
    var toggleButton = document.getElementById("toggleButton");
    var toggle = false;
    var switchCount = 0;

    function switchLinks() {
        if (toggle) {
            // Swap the href attributes back to their original values
            link1.href = "https://www.ulta.com/p/luna-rossa-black-eau-de-parfum-xlsImpprod18731053";
            link2.href = "https://www.fragrantica.com/perfume/Prada/Luna-Rossa-Black-48682.html";
            toggleButton.textContent = "Switch Links";
            link1.textContent = "Ingredients";
            link2.textContent = "Prada Black Scent Profile";
        } else {
            // Swap the href attributes
            var tempHref = link1.href;
            link1.href = link2.href;
            link2.href = tempHref;
            toggleButton.textContent = "Switch Links";
            if (link1.textContent === "Ingredients") {
                link1.textContent = "Prada Black Scent Profile";
                link2.textContent = "Ingredients";
            } else {
                link1.textContent = "Ingredients";
                link2.textContent = "Prada Black Scent Profile";
            }
        }
        toggle = !toggle;

        // Update the switch count
        switchCount++;
        document.getElementById("switchCount").textContent = switchCount;

        // Update the displayed links
        document.getElementById("link1Text").textContent = link1.textContent;
        document.getElementById("link2Text").textContent = link2.textContent;
    }
</script>
