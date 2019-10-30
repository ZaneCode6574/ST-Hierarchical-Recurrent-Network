# Introduction
The primary goal of skeletal motion prediction is to generate future motion by observing a sequence of 3D skeletons.A key challenge in motion prediction is the fact that a motion can often be performed in several different ways, with each consisting of its own configuration of poses and their spatio-temporal dependencies, and as a result, the predicted poses often converge to the motionless poses or non-human like motions in long-term prediction.This leads us to define a hierarchical recurrent network model that explicitly characterizes these internal configurations of poses and their local and global spatio-temporal dependencies. The model introduces a latent vector variable from the Lie algebra to represent spatial and temporal relations simultaneously. Furthermore, a structured stack LSTM-based decoder is devised to decode the predicted pose with a new loss function defined to estimate the quantized weight of each body part in the pose. Empirical evaluations on benchmark dataset suggest our approach significantly outperforms the state-of-the-art methods on both short-term and long-term motion prediction.


# Visualization of long-term prediction

&nbsp;&nbsp;

### Walking


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/OY4bcDJfJeY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

### Posing


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/UptXczFf6Ro" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

### Eating


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/RDFGcYIzYuw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

# Results on short-term prediction

