# Generating Adversarial inputs for LPR systems(DSCI-6672-AI-DS-Cyber-Security-Final Project)
#Generating adverserial inputs for License plate recognition systems

Final Project for  DSCI-6672-AI-DS-Cyber-Security- University of New Haven

Introduction:

This Project consists of the License plate Recognition Models and then perturbing a individual integer as an input for adversarial attacks.

The dataset is ReID and is explained detailly below.

The image processing techniques have been adapted from several scholars of github .



I have tried to perturb the whole license plate in as a single input but due to some technical limitations as of now for the strides . Unable to convert strides of 3 or 1 to 2.

So instead we go with the process of perturbing the sgregated images.
Segregated images are individual images that are segregated form license plates . They are cleaned filtered and then segregated. This model is adverserially attacked if we can paste the perturbed images shown in the ipynb onto a valid license plate. And we should test the plate with the same model not any other model. 

As we have created the perturbation based on the model this wpould be considered white box attack .


# Next steps

The next steps would be to make this a black box attack if possible and do it for the complete license plate as input instead of the segregated images of each.

         



