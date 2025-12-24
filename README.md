                                             THIS REPO USES
Data Extraction: I utilized a YOLO model to track players in both the broadcast and tactical feeds, saving all tracking data (bounding boxes and IDs) into separate CSV files (cam_1 and cam_2).

Shot Analysis: I analyzed the number of players detected per frame to identify sudden jumps in the broadcast feed, allowing the system to distinguish between wide shots and close-ups.

Synchronization: To align the timelines, I chopped 3 seconds from the start of the tactical camera footage and updated the tracking data into a synchronized file (cam_2_synched).

Matching & Voting: I performed topological matching based on the relative spatial order of players. I used a voting mechanism to establish confidence, discarding any matches with fewer than 10 votes.

Visualization: Finally, I generated final_solution.mp4, where matched players are labeled with consistent colors to verify the solution.

THE CODE CELLS HAVE A BRIEF DESCRIPTION OF WHATS HAPPENING IN EACH CELL, GIVING A GOOD UNDERSTANDING OF THE CODE.



https://github.com/user-attachments/assets/9378591e-153b-43ad-9e25-3692ceb2062b


## 🛠 Dependencies & Environment

To run this notebook, you need a Python environment with the following libraries installed.

**Required Libraries:**
* `ultralytics` (YOLOv8)
* `opencv-python` (cv2)
* `pandas`
* `matplotlib`
* `numpy`

/content/drive/MyDrive/objecttracking/
├── best.pt
├── tacticam.mp4
└── broadcast.mp4

If you are running this locally or need to reinstall in Colab, run:
```bash
pip install ultralytics opencv-python pandas matplotlib numpy                                        
