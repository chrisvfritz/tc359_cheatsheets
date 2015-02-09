CSS Pseudo Elements

CSS pseudo elements are similar to pseudo classes, but they are a little different. Pseudo elements allow you to style certain parts of the document. You do this by attaching the specific pseudo element to the selector you would like to style.

    Some main CSS pseudo elements are:

        ::after
        ::before
        ::first-letter
        ::first-line


The ::after pseudo element allows you to add additional cosmetic content after the selector that it is attached to and it is set up to be inline by default.

Format:

    element::after { CSS properties }

Example:

    HTML:

        <p class="text">This is a line of text.</p>

    CSS:

        .text::after {
            content: "Adding some additional content after the sentence.";
            color: green;
        }

    Result:

        The line of HTML text will be displayed, then the additional line of text will be displayed just right of it in a different color.


The ::before pseudo element does the same thing as the after element, but it adds the cosmetic content to the beginning of the selector. This element is also inline by default.

Format:

    element::before { CSS properties }

    h1::before { CSS properties }

Example: 

    HTML:

        <h1>This is a Headline!!</h1>
        <p class="text">This is a line of text.</p>

    CSS:

        h1::before {
            content: "Hello!";
            color: red;
        }

        .text::before {
            content: "Adding some additional content after the sentence.";
            color: green;
        }

    Result:

        The header will be displayed just to the right of the "Hello!" listed in the h1::before section. Same thing will happen for the lines of text as it did in the ::after example, except the additional line of text will be displayed on the left this time.


The ::first-letter pseudo element selects the first letter of the first line of a block. This only works if it does not follow any other content on the same line. This element only affects sections with a display value of block, inline-block, table-cell, list-item, or table-caption. If it is displayed as anything else, ::first-letter will not work.

Example:

    CSS:

        p::first-letter {
            color: orange;
            font-size: 150%;
        }

    Result:

        This CSS will take the first letter of every paragraph and it will change the color to orange and it will increase the font size to 150%.


The ::first-line pseudo element is very similar to the ::first-letter element except that it applies the changes to the entire first line of the selection, not just the first letter. This element only affects sections with a display value of block, inline-block, table-cell, or table-caption. If it is displayed as anything else, ::first-line will not work.

Example:

    CSS:

        p::first-line {
            color: blue;
            text-transform: uppercase;
        }

    Result:

        This CSS will take the entire first line of every paragraph and make all the letters change to blue and it will also make them all uppercase.


For more examples on CSS pseudo elements and to find a few more useful tips visit this site:

    https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements