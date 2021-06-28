## IMU-TL: Transfer Learning for Inertial-based Activity Recognition 
This repository provides a framework for evaluating the benefits and limitations of Transfer Learning for 
Inertial-based Activity Recognition. 

### Configuration Parameters
Parameter Name | Description |
--- | --- |
General parameters|
n_freq_print|How often to print the loss to the log file
n_freq_checkpoint|How often to save a checkpoint
n_workers|Number of workers
device_id|The identifier of the torch device (e.g., cuda:0)
Data parameters|
input_dim|The dimension of the input IMU data, e.g., 6 when using accelerometers and gyros
window_size|The size of the time window (i.e. how many samples in a window)
num_classes|Number of classes
window_shift|The window shift, put here the window_size to avoid window overlap
Training hyper-parameters|
batch_size| The batch size
lr|The learning rate
weight_decay|The weight decay 
eps| epsilon for Adam optimizer
lr_scheduler_step_size|How often to decay the learning rate
lr_scheduler_gamma|By what factor to decay the learning rate
n_epochs|Number of epochs
Transformer architecture hyper-parameters|
encode_position|Whether to encode positions for IMU-Transformer
transformer_dim|The latent dimension of the Transformer Encoder
nhead|Number of heads for the MHA operation
num_encoder_layers| Number of encoder layers (Transformer)
dim_feedforward:| The latent dimension of the Encoder's MLP
transformer_dropout| The dropout applied to the Transformer
transformer_activation| Activation function used for the Transformer (gelu/relu/elu)
head_activation|Activation function used for the MLP classifier head 
CNN architecture hyper-parameters|
dropout| Dropout applied for the CNN model
latent_dim| Dimension of the latent convolution layer 


