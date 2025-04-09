** This creates a rating system where: --> **
    Clicking a star highlights that star and all previous stars
    Emojis slide into view and change color based on the rating
    Colors progress from "red" (bad) to "green" (good)
    Initial state shows no stars selected (rating of 0)


**Star Updates:--> **
Loops through all stars
    If the star's index is less than index + 1, adds "active" class (fills the star)
    Otherwise, removes "active" class (empties the star)
    Example: If index is 2, stars 0, 1, and 2 get "active", others don't

**Emoji Updates:--> **
Loops through all emojis
    Moves them horizontally using translateX by -index * 50 pixels
    Sets their color based on the corresponding value in colorsArray
    The negative translation moves emojis left as the rating increases

**How It Works Together:--> ** Imagine 5 stars and 5 emojis in the HTML
Clicking star 3 (index 2):
    Stars 0, 1, and 2 get "active" class (typically making them filled/yellow)
    Stars 3 and 4 lose "active" class
    All emojis move left by -100px (2 * 50)
    All emojis turn lightblue (colorsArray[2])

