
Ball Tracking in Quadrants
---
Overview
--
This project involves tracking the movement of colored balls (yellow, green, white, and orange) across predefined quadrants in a video. The program records each ball's entry and exit events along with their timestamps. The output includes a processed video with overlays and a text file logging the events.

Dependencies
---
opencv-python==4.5.3.56

numpy==1.21.1

Installation
---
To install the necessary dependencies.

python process_video.py
---
The processed video will be saved as output_video.mp4 and the event log will be saved as output_events.txt.

Code Explanation
--
1. Color Detection
   
The define_color_ranges function defines HSV color ranges for detecting yellow, green, white, and orange balls.

3. Quadrant Definition
   
The define_quadrants function defines the quadrants within the video frame and shifts them to the right for accurate tracking.

5. Ball Tracking
The detect_balls function uses contour detection and morphological operations to identify balls in the frame. The get_quadrant function determines the quadrant of a detected ball.

6. Event Logging
Events are recorded with the format Time, Quadrant Number, Ball Color, Event Type (Entry/Exit). These events are written to a text file.

7. Output
The processed video includes overlays for ball tracking, event logging, and timestamps. The results are saved to output_video.mp4 and output_events.txt.

Files
---
process_video.py: Main script for processing the video.

requirements.txt: List of dependencies.

output_video.mp4: Processed video with overlays.

output_events.txt: Log of ball movement events.

Sample Output
---
The processed video displays the following:

Quadrant grid.
--

Detected balls with color identification.

Entry and exit events with timestamps.

The text file logs events in the following format:

