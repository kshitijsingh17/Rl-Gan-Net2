# RL-Gan-Net
Reimplementation of RL-GAN-Net: A Reinforcement Learning Agent Controlled GAN Network for Real-Time Point Cloud Shape Completion (https://arxiv.org/pdf/1904.12304v1.pdf) Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2019

The official repository of the paper can be found here: https://github.com/iSarmad/RL-GAN-Net

## Dataset
The point cloud dataset is publicly available and can be downloaded from the following link: https://github.com/optas/latent_3d_points
In our experiments, we work on a subset of 5000 point clouds.'generate_noisy_point_clouds.py' creates a noisy point cloud for each. This is done by initializing a random seed index and removing 20 percent of points following the seed index.

## Training of Autoencoder
The complete code for dataloader, encoder-decoder models, chamfer loss and training is present in 'autoencoder.ipynb'. In the results folder, we have added the loss plots and some results of the trained autoencoder. 

### AE Results
The following some generated samples from the trained AE:

![screenshot](https://github.com/kshitijsingh17/Rl-Gan-Net2/blob/main/ae_results.png)

## Training of GAN
The complete code for dataloader, generator, discriminator models and training is present in 'gan.ipynb'. In the original paper, the noise vector input to the generator is a 32-dimensional normal random variable however in our experiments we were able to reproduce the results with 5-dimensional noise vector. Some results and loss plots of both generator and discriminator are present in the results folder for reference.

### GAN Results
The following some generated samples from the trained GAN:

![screenshot](https://github.com/kshitijsingh17/Rl-Gan-Net2/blob/main/gan_results.png)

## Training of RL-Agent
The complete code for actor, critic networks, DDPG and training code is present in the 'rl_agent_classes_only'. Some results and reward plots for the agent are present in the results folder for reference (https://drive.google.com/drive/folders/1mmJp4Fa0wGIXImQ9Jz9h1vTcAmpgmw-l?usp=sharing)


## Results
The followiong are some results for RL-GAN-Net (left: incomplete point cloud, right: generated output)

![screenshot](https://github.com/kshitijsingh17/Rl-Gan-Net2/blob/main/results.png)

## Observations
We found that the final output is highly sensitive to the weights assigned to each reward. We had to run a lot of experiments to get some meaningful results

###### Team Members: Kshitij Singh, Pranav, Shubham Singh
 

