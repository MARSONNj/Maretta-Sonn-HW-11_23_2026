# DotStimVisual: Random-Dot Motion Task

This PsychoPy experiment measures how well a participant can tell the direction of moving dots. A Python script then graphs their accuracy across the trials.

## The task

Each trial shows a field of 150 dots. A proportion of the dots, called the coherence, moves together in one direction, either left or right. The remaining dots move randomly as noise. Participants press the left or right arrow key to indicate the direction of the moving dots. Coherence ranges from 5% to 80%, so low levels are hard to judge and high levels are easy. Each trial starts with a fixation cross shown for a random 0.5 to 1.5 seconds.

## Requirements

- Python 3 with PsychoPy, pandas, and matplotlib installed.

## How to run it

1. Install PsychoPy, pandas, and matplotlib.
2. Open `DotStimVisual.py` in PsychoPy Runner.
3. Press the Run button.
4. In the dialog box, enter the participant number and age, then choose the number of trials (10, 50, 100, or 150).
5. Press Return on the instructions screen to start.
6. On each trial, press the left or right arrow key. Press Escape to quit early.

## What gets saved

After a run, the script saves two files in the same folder as the script. Both file names start with the participant number.

- **`[participant number]_random_dot_motion.xlsx`** holds the trial settings and timing, including coherence, direction, the correct response for each trial, and fixation duration.
- **`[participant number]_random_dot_motion_responses.csv`** holds what the participant did on each trial. Its columns are:
  - `direction`: 0 for right, 180 for left
  - `coherence`: the proportion of dots moving together
  - `correct`: True if the participant's response matched the direction, otherwise False
  - `resp`: the key the participant pressed
  - `rt`: reaction time in seconds
  - `fixation_dur`: the length of the fixation cross on that trial, in seconds
  - `trial_number`: the order of the trial, starting at 1

## What the graph shows

After the experiment ends, the script shows a line graph of accuracy across the trials. The x-axis is the trial number, and the y-axis is the proportion of correct responses, averaged over each run of 10 trials. The dashed line marks chance (50%). A participant who is guessing would have a line that stays near the dashed line, while a participant who can see the motion would have a line above it. Close the graph window to end the script.
