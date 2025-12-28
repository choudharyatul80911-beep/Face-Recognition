# Face-Recognition
Face Recognition based on Raspberry Pi 5 and Webcam
# Face Recognition on Raspberry Pi (Webcam Version)

This project demonstrates a live Face Recognition system running on a Raspberry Pi using a USB Webcam. It uses OpenCV and Python to detect faces, train a model on specific individuals, and identify them in real-time.

This project is a customized implementation inspired by [Caroline Dunn's Facial Recognition project](https://github.com/carolinedunn/facial_recognition).

## Features
- **Data Collection:** Capture headshots using a USB Webcam to create a dataset.
- **Model Training:** Train a recognizer model based on the captured images.
- **Real-time Recognition:** Identify users (e.g., "Atul") via a live video feed with FPS display.

## Hardware Requirements
- Raspberry Pi 4 (or 5) recommended for better FPS.
- USB Webcam (e.g., Logitech C270 or similar).
- MicroSD Card (16GB+ recommended).
- Monitor, Keyboard, and Mouse for setup.

## Software Prerequisites
- Raspberry Pi OS (Legacy or Bullseye recommended for camera compatibility).
- Python 3
- OpenCV
- dlib
- face_recognition library

## Installation


1. **Update system**
   ```bash
      sudo apt-get update
      sudo apt-get upgrade


2. **Set up Virtual Environment and Install Libraries**
   
     ```bash
   python3 -m venv --system-site-packages face_rec
3. **Activate the virtual environment**
   
    ```bash
     source face_rec/bin/activate
4. **Add Swap Memory**

   The Raspberry Pi doesn't have enough memory to complile dlib. Add swap space to avoide memory crashes during compilation
   
   ```bash

         sudo nano /etc/dphys-swapfile
5. **Find the line**

    ```bash
            
            CONF_SWAPSIZE=512

6. **Change it to**
   
   ```bash

            CONF_SWAPSIZE=2048
   
**Save and exit (CTRL+X, then Y, Then Enter), then restart the swap service**

    
        sudo systemctl restart dphys-swapfile
7. **Install Required Python Libraries**
    ```bash
    pip install opencv-python
    pip install imutils
    sudo apt install cmake -y
    pip install face-recognition


**Once you're done with installation, it's a good idea to change the swap size bac to reduce SD card wear**

    sudo nano /etc/dphys-swapfile
8. **Find the line**

    ```bash
            
     CONF_SWAPSIZE=2048

9. **Change it to**
   
    ```bash

    CONF_SWAPSIZE=512

10. **Then restart the service** 
          
    
           sudo systemctl restart dphys-swapfile
           
11. **Download the Code**
      ```bash
           https://github.com/choudharyatul80911-beep/Face-Recognition.git
      
12. **Change into the directory**
    ```bash
            cd facial_recognition
       
13. **Delete the sample directory**
       ```bash
        rm -r dataset/Z
14. **Headshots**
       ```bash
       nano headshots_capture-webcam.py
 15. **Change line 7 of the file replacing YOUR_NAME**
        ```bash
        YOUR_NAME=''YOUR_NAME''
 16. **Save and exit by pressing Ctrl+X, then Y, and hit Enter**

     
 17. **Now run the script for the webcam**
        ```bash
        python3 headshots_capture-webcam.py

        
 **Look at the camera and press the spacebar to take photos. Move your head around and take at least 10 photos.**

 
 **Press q to exit . Repeat this for each person**
 
 **You should now see a folder for each person with a set of headshots**

 
18. **Train the Model**
 
      ```bash
      python3 model_training.py

   If successful, you will get a .pickle file.

19. **Run the Facial Recognition Test**
       ```bash
       python3 face_rec-webcam.py
 Press **q** to exit.      


****Set Up & Hardware**** 
[Hardware&Setup] (Setup_Hardware.jpeg)
