# Generating Recognizable Long-term Articulated Objects Motion via Hierarchical Recurrent Network

## Introduction
The primary goal of articulated object motion prediction is to generate future motion by observing sequence of 3D skeletons. Currently, people focus on creatures such as human and animals motion prediction. As we scrutinized current methods, we found that previous workings always focused on the temporal angle, which ignores the fine-grained spatial aspect and the inner relationship of one pose. Meanwhile, state-of-art models only obtained well results on simple activities for long-term prediction. To dig out the reasons behind this and address these problems, we proposed a novel spatio-temporal hierarchical recurrent network, which can simultaneously model local and global sptio-temporal context. Furthermore, a structured stack LSTM decoder is used to obtain spine, arm, and leg respectively. In the end, a novel loss function is introduced to compute a quantized weight for each bone of one pose. Extensive experiments demonstrated the superiority of our model on both short-term and long-term motion prediction over state-of-art models.

## Visualization of long-term prediction

### Walking
### Posing
### Greeting

## Results on short-term prediction
