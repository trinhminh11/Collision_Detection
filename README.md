# How to use
1. Download data from https://www.kaggle.com/datasets/minhtrnhth/collision-detection
2. Put all video to folder `data`
3. run all cell in `data_processing.ipynb` to create `train_tensor`, `val_tensor`, `train.csv` and `val.csv`
4. run all cell in `model.ipynb`

# Overview
The Car Collision Detection project leverages deep learning techniques to identify collisions in video data. The system is designed to:

1. Utilize any backbone vision model for feature extraction, with the current implementation using InceptionV3.
2. Process video inputs by reading them into a 16-frame sequence spread evenly across the video.
3. Generate 17 output features, where:
    - The first 16 features indicate the frame where a collision occurs.
    - The 17th feature is a binary indicator (1 if a collision is detected, 0 otherwise).
4. The model outputs `-1, -1` if no collision is detected (i.e., the 17th feature is 0). If a collision is detected (i.e., the 17th feature is 1), the output specifies the time window during which the collision occurs.
