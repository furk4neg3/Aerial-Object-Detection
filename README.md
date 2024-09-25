# Information About the Project
-> This project is focused on aerial object detection. Dataset is SkyFusion that contains satelite images. Task is to draw border box around objects and classify them. 

-> Because the photos were taken from a distance, objects look small, so that makes it a hard challenge.

-> I used PyTorch to create AI models. Making the model flexible for varying number of boxes in images was the biggest challenge.

-> Created one model from scratch myself. Backbone uses concolutional layers for learning, and pooling layers etc. for better performance. Then model gets to 2 heads. 1 creates border box output, other one makes classification. In classification head, I used linear layers too. 

-> Used a custom loss function to train these, border box's loss is calculated by smooth l1 loss and classification's loss is calculated by cross entropy loss.

-> Then I used transfer learning. Fast RCNN model was one of the best choices for this challenge, so I chose it. Tried to fine tuned it too but when training I had problems with hardware capabilites so commented out that part.

-> Fast RCNN model worked with 0.8746 loss. That's a pretty good result for object detection, especially when objects seem small in images because the photos were taken from a distance.
