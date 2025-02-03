**Demo Image**

![image](https://github.com/user-attachments/assets/5a999b74-c82b-4300-baca-5e3b1255e466)

### **Drowsiness Detection System – Overview**  

1. **Purpose**: Detects driver drowsiness in real time using facial landmarks and Eye Aspect Ratio (EAR). Triggers an alarm when drowsiness is detected.  
2. **Technologies Used**: Python, OpenCV, dlib (facial landmarks), imutils, scipy, playsound.  
3. **How It Works**:  
   - Uses dlib’s **68 facial landmark model** to detect eyes.  
   - Calculates **EAR** to determine eye openness.  
   - If EAR < 0.3 for **48 frames**, triggers an **alarm**.  
   - Also detects **blinking** (20 frames).  
4. **Key Features**:  
   - **Real-time video processing**.  
   - **Adjustable EAR threshold & frame count**.  
   - **Visual feedback & alarm system**.  
5. **Exit**: Press **'q'** to quit.  

### **Steps to Run**  

1. **Install Dependencies**  
   ```bash
   pip install opencv-python imutils dlib scipy playsound argparse numpy
   ```  
2. **Download dlib’s Facial Landmark Predictor**  
   - Get `shape_predictor_68_face_landmarks.dat` from [dlib's model repository](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2).  
   - Extract it to the project folder.  

3. **Run the Script**  
   ```bash
   python detect_drowsiness.py --landmark-identifier shape_predictor_68_face_landmarks.dat
   ```  
   - To enable alarm sound:  
     ```bash
     python detect_drowsiness.py --landmark-identifier shape_predictor_68_face_landmarks.dat --alarm alarm.wav
     ```  
