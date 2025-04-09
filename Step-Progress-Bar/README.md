Welcome to the Step Progress Bar Project! The final version includes five steps. We also have previous and next buttons. Initially, the previous button is disabled as we cannot go back to any previous step yet. Clicking on the next button displays the first step and enables the previous button. As we continue clicking on the next button, we move forward to each step until we reach the final step, after which the next button becomes disabled. We can move back to any previous step by clicking on the previous button. Inactive steps are greyed out with a cross icon, but when activated, they turn green with a check icon. The JavaScript dynamically displays the number of each step.


**variable setup --> ** 
    "Next" button: Increases currentChecked, prevents exceeding total steps
    "Prev" button: Decreases currentChecked, prevents going below 1
    Both call updateStepProgress() to refresh the UI

**Event Listeners --> **
    Selects HTML elements using DOM methods
    stepsEl is a NodeList of all elements with class "step"
    currentChecked keeps track of progress (1-based indexing)

**Step Visual Update --> **
Loops through each step element
For completed steps (idx < currentChecked):
    Adds "checked" class
    Inserts a checkmark and text ("Start" for first, "Final" for last, "Step X" for others)
For uncompleted steps:
    Removes "checked" class
    Shows an X icon


**Progress Bar Update --> **
    Counts elements with "checked" class
    Calculates percentage: (completed - 1) / (total - 1) * 100
    Sets progress bar width (0% at start, 100% when all steps complete)

**Button State Update --> **
    Disables "Prev" at first step
    Disables "Next" at last step
    Enables both for middle steps



