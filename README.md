# GAN_CNN

What is Generative Adversial Network(GAN)    
GAN attacks the problem of unsupervised learning by training two deep networks, called Generator and Discriminator, that compete and cooperate with each other. In the course of training, both networks eventually learn how to perform their tasks.    

Generative Adversial Network Consists of 2 Networks:    
– Generator (Criminal) and Discriminator (Police)

• The responsibility of each network:    
  – Criminal tries to produce "counterfeit" output to trick police    
  – Police examines "counterfeit" output and rates how real or fake it is    
  – Criminal tries to improve its authenticity score    
  – Police tries to improve its detection of real vs fake    
  
What can we do with GANS?    
• Generate new images for data for training    
• Generate photos of human faces    
• Generate matching shoes for a given accessory    
• Face Aging    
• Convert Drawing Outline / Segment Map to Photograph    
• Increasing an Image Resolution    
• Data Augmentation?   
• And lots more…    


GAN Training consists of the following steps:  
  1) Use generator to generate fake images
  2) Use real + generated fake images to train discriminator as a classifier
  3) Initialize a fixed set of random noise at Generator
  4) Train the generator weights to produce fake data that will trick discriminator into thinking that they are real
  5) When the final generator model is able to fool the discriminator, we can discard the discriminator. We use the generator used to generate new images
  
GAN Training    
  – Discriminator trains for >= 1 epochs    
  – Generator trains for >= 1 epochs    
  – Repeat until when the Discriminator's accuracy on the fake images near 0.5    
  (means the Discriminator has a hard time telling if the generated output is real or fake)    
  
  • Use only the Generator for generating new outputs
  
 
Challenges in GAN
•	GAN is simple in theory, it is very difficult to build a model that works. 

•	In GAN, there are two deep networks coupled together making back propagation of gradients twice as challenging


Its advisable to reuse existing GAN model


