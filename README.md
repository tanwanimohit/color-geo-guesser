# Color Geo Guesser

A fun and challenging web-based game designed to test and improve your color perception. See a color, pick your guess from an interactive color wheel, and get a score based on how close you are!

![Screenshot of the Color Guesser Game](https://placehold.co/800x450/e2e8f0/4a5568?text=Game+Screenshot+Here)

---

## How to Play

1.  A random color will be displayed in the "Match this Color" box on the left.
2.  Use the interactive color picker on the right to select the color you think matches the target.
3.  The "Guess" button will change color in real-time to match your selection.
4.  Once you're happy with your choice, click the **Guess** button.
5.  Your score will be displayed, showing how close your guess was to the actual color. You'll also see a side-by-side comparison.
6.  Click **Next Round** to try again with a new color!

---

## Features

-   **Accurate Perceptual Scoring**: Uses the **CIELAB color space (Delta E 1976)** to calculate a score that truly reflects how humans perceive color differences.
-   **Interactive Color Picker**: Powered by the smooth and modern **iro.js** library for an intuitive user experience.
-   **Dynamic UI**: The "Guess" button instantly updates its background color and text contrast as you make a selection.
-   **Responsive Design**: A clean, mobile-first layout built with **Tailwind CSS** that looks great on any device.
-   **Instant Feedback**: Get immediate results with a percentage score, a visual comparison of the colors, and a fun feedback message.
-   **Self-Contained**: No complex setup required. The entire game runs from a single HTML file.

---

## Technical Details

### Scoring Logic

Instead of relying on a simple RGB distance, which doesn't align well with human perception, this game implements a more advanced scoring model:

1.  Both the target and guessed hex colors are converted to the **RGB** color model.
2.  The RGB values are then converted to the **CIELAB** color space. CIELAB is designed to be perceptually uniform, meaning a numerical change in color values corresponds to a similar perceived change in color.
3.  The distance between the two LAB colors is calculated using the **Delta E 1976** formula.
4.  This distance (where a smaller number means a closer match) is converted into a percentage score from 0% to 100%.

### Tech Stack

-   **HTML5**: For the core structure of the game.
-   **Tailwind CSS**: For a utility-first, responsive, and modern design.
-   **JavaScript (ES6+)**: For all game logic, DOM manipulation, and event handling.
-   **[iro.js](https://iro.js.org/)**: A powerful, SVG-based color picker library.

---

## How to Run Locally

1.  Download the `index.html` file.
2.  Open the file directly in any modern web browser (like Chrome, Firefox, or Edge).
3.  That's it! No web server or installation is needed.

---

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).