
# Finger Detection and Counting

This project utilizes computer vision techniques to detect and count fingers in a live video stream. It segments the hand region from the background, calculates the convex hull of the hand, and then counts the number of fingers based on the convexity defects.

![image](https://github.com/Jakhmola/Finger_Count/blob/main/Finger_count.png)

## Dependencies

This project requires the following Python libraries:

- `cv2`: OpenCV for image processing
- `numpy`: Numerical operations
- `sklearn`: For distance calculation

Ensure these dependencies are installed in your Python environment before running the project.

## Getting Started

1. **Clone the Repository**: Clone this repository to your local machine.

2. **Install Dependencies**: Install the required dependencies using pip or conda.

3. **Run the Program**: Execute the `finger_detection.py` script to start the finger detection and counting process.

## Usage

Upon running the program, a live video stream will open showing the detected hand and the count of fingers. 

- **Background Calibration**: The program initially calibrates by capturing the background for the first 60 frames. During this period, ensure there are no hands in the frame.

- **Hand Detection**: Once the background is calibrated, the program detects and segments the hand region from the background.

- **Finger Counting**: Using convex hull and convexity defects, the program counts the number of fingers raised.

- **Exit**: Press the `Esc` key to exit the program.

## Customization

You can customize the following parameters in the script:

- `roi_top`, `roi_bottom`, `roi_left`, `roi_right`: Region of interest (ROI) for hand detection.
- `accumulated_weight`: Weight for accumulating background.
- `threshold`: Threshold value for segmenting hand region.
- `num_frames`: Number of frames for background calibration.

Feel free to adjust these parameters according to your requirements.
