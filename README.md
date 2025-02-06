# UE4 Generated Fall Detection Dataset

## 📌 Introduction
As the global population ages, fall detection has become a crucial issue in elderly care. Existing fall detection datasets are often limited in scale, diversity, and real-world applicability due to privacy concerns and data collection challenges. 

This dataset, **generated using Unreal Engine 4 (UE4)**, provides a large-scale, photorealistic synthetic dataset of **fall and non-fall** actions to facilitate research in **computer vision-based accident detection**. By leveraging **3D virtual environments and physics simulations**, we create diverse and realistic fall scenarios, addressing common dataset limitations such as **occlusion, camera angles, and environmental complexity**.

This dataset is intended for use in **human action recognition, pose estimation, and accident detection models**, particularly for deep learning-based solutions.

---



## 📥 Download Dataset
[Click here to download the dataset (Google Drive)](https://drive.google.com/file/d/1c_UirWUuqJPMAohLENPUDOVuBbPIrArE/view?usp=sharing)

---

## 📊 Dataset Overview
- `Total Videos`: 1000 (including falls and non-falls)
  - `Fall Types`:
      - stumbling
      - slipping
      - fainting
  - `Non-Fall Actions`:
    - sleeping
    - kneeling
- `Camera Views`: Multi-angle 
- `Resolution`: 640×480
- `Frame Rate`: 10 FPS

---

## 📂 Dataset Structure
The dataset consists of **falling actions and confusing non-fall actions** recorded from multiple camera angles. It is organized as follows:




```markdown
📂 UE4_Fall_Detection_Dataset/
├── 📂 data/                    
│    ├── 📂 fall_samples/     
│    │    ├── 📂 Faint/
│    │    │    ├── 📂 Images/
│    │    │    ├── 📂 Camera_traj/
│    │    │    ├── 📂 Skeleton_traj/
│    │    ├── 📂 Stumble/
│    │    ├── 📂 Slip/
│    │    ├── 📂 non_fall_samples/ 
│    │    │    ├── 📂 Sleep/
│    │    │    ├── 📂 Kneel/  
├── README.md                
├── LICENSE                                       

```

---

## 📝 Data Format
The dataset includes **videos and corresponding annotations**:

- **Videos**: `.mp4` files of human actions (falling & non-falling)
- **Annotations (`annotations.csv`)**:
  - `filename`: Name of the video file
  - `label`: Action category (`fall` or `non_fall`)
  - `timestamp`: Fall event timestamp (if applicable)
  - `camera_angle`: Camera perspective (e.g., `front`, `side`, `top`)
  
---


### 📄 Frame-by-Frame Images (frames/*.jpg)
Each action sequence is stored as sequential image frames, named following:

`{camera_id}_{action_number}_{frame}_{task}.jpg.`



🔹 **Format Details**
- `Resolution`: 640×480 pixels 
- `Frame Rate (FPS)`: 10 
- `File Type`: .jpg
---
### 📄 Camera Tragedy (camera/*.json)
Each sequence includes a camera parameter file

📌 **Example Format** `cam_pose_1.json`
```markdown
[
    {
        "frame": 1,
        "cam_id": 1,
        "location":[
            1824.0,
            1434.0,
            295.0
        ],
        "rotation":[
            -30.0,
            50.0,
            0.0
        ]
    },
    ...
]
```
🔹 **Format Details**
- `frame`: Frame Number 
- `camera_id`: Camera Number
- `position`: 3D coordinates (X, Y, Z)
- `rotation`: Rotation angles (Yaw, Pitch, Roll)
---
### 📄 3D Skeleton Data (skeletons/*.json)
Each frame contains 3D skeleton keypoints, stored as JSON.

📌 **Example Format** `skeleton_1.json`
```markdown
[
    {
        "frame": 1,
        "skeleton": {
            "Root": {
                "Pitch":0.0.,
                "Yaw":0.0,
                "Roll":0.0,
                "X":0.0,
                "Y":0.0,
                "Z":0.0,
                "ScaleX":1.0,
                "ScaleY":1.0,
                "ScaleZ":1.0
            },
            ...

        }
    }
   
]
```
---
## 🔬 Data Generation Methodology
The dataset was generated using Unreal Engine 4 (UE4) and UnrealCV, allowing us to:

- Create photorealistic 3D virtual environments with realistic lighting, furniture, and obstacles.
- Simulate natural human movements using AI-controlled character physics.
- Capture multi-view video sequences with automatic camera placement.
- Export ground-truth 3D skeletons and physical movement data for model training.



---


## 📜 License
This dataset is licensed under Creative Commons Attribution 4.0 International (CC BY 4.0). You are free to:

Share: Copy and redistribute the material.
Adapt: Remix, transform, and build upon it. Attribution is required—please cite our work when using this dataset.


---
## 📬 Contact
For inquiries, please contact:

Caroline Huang (📧 carolinehuang0303@gmail.com)


