# Information of Project
-> This project is focused on aerial object detection. Dataset is SkyFusion that contains satelite images. Task is to draw border box around objects and classify them. 

-> Because the photos were taken from a distance, objects look small, so that makes it a hard challenge.

-> I used PyTorch to create AI models. Making the model flexible for varying number of boxes in images was the biggest challenge.

-> Created one model from scratch myself. Backbone uses concolutional layers for learning, and pooling layers etc. for better performance. Then model gets to 2 heads. 1 creates border box output, other one makes classification. In classification head, I used linear layers too. 

-> Used a custom loss function to train these, border box's loss is calculated by smooth l1 loss and classification's loss is calculated by cross entropy loss.

-> Then I used transfer learning. Fast RCNN model was one of the best choices for this challenge, so I chose it. Tried to fine tune it too, but hardware didn't allow it.


# Note:
There are some issues in the notebook (mainly visualization, like it has to count from 1 to 10 but counts 0 to 9). These will be fixed soon, check again in 1-2 days for fully completed version. Planning to add some examples of how models make predictions on example images too.
