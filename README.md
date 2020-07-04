# Age Recognition on Facial Images
Modified VGG-16 NN that detects a person's age from facial images.
### Dataset
The dataset used in this project is the IMDB-Wiki faces dataset, which originally contains over 60,000 facial images. Since some of the images are either not relevant (not facial image) or unclear (can be too small, blur, etc), over 15,000 images are removed, which left about 45,000 filtered images as training data. Data augmentation is implemented.
### Neural Network
The neural network is a modified VGG-16 network, which an extra global average pooling (GAP) layer is added before the Dense layer. Grad-CAM method is applied to visualize the neural network.
### Result
- The MAE for original VGG16 structure with original dataset is around 15.
- The MAE for VGG16-GAP network with processed and augmented dataset is 9.75.
- The model makes good age prediction for images in age groups ranging from 20-50.
- The model is paying more attention to the central area of human faces (such as nose, mouth, forehead) in successful predictions. For example, elder people tends to have white hairs and mustache, while younger people have less wrinkles on their face.
- Background is sometimes misleading. The model tends to look at background in the failure predictions.
