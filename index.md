# Introduction
The primary goal of articulated object motion prediction is to generate future motion by observing sequence of 3D skeletons. Currently, people focus on creatures such as human and animals motion prediction. As we scrutinized current methods, we found that previous workings always focused on the temporal angle, which ignores the fine-grained spatial aspect and the inner relationship of one pose. Meanwhile, state-of-art models only obtained well results on simple activities for long-term prediction. To dig out the reasons behind this and address these problems, we proposed a novel spatio-temporal hierarchical recurrent network, which can simultaneously model local and global sptio-temporal context. Furthermore, a structured stack LSTM decoder is used to obtain spine, arm, and leg respectively. In the end, a novel loss function is introduced to compute a quantized weight for each bone of one pose. Extensive experiments demonstrated the superiority of our model on both short-term and long-term motion prediction over state-of-art models.

# Visualization of long-term prediction

&nbsp;&nbsp;

## Walking


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/4Z1IWTl-_7w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

## Posing


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/UptXczFf6Ro" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

## Eating


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/Scur-WShQ5Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

&nbsp;

# Results on short-term prediction

<table>
    <tr>
        <td rowspan=2>Methods</td>
        <td colspan=8>Directions</td>
    </tr>
    <tr>
        <td><B>80ms</B></td>
        <td>160ms</td>
        <td>320ms</td>
        <td>400ms</td>
        <td>560ms</td>
        <td>640ms</td>
        <td>720ms</td>
        <td>1000ms</td>
    </tr>
    <tr>
        <td>ST_HMR</td>
        <td>0.41</td>
        <td>0.58</td>
        <td>0.78</td>
        <td>0.86</td>
        <td>0.98</td>
        <td>1.04</td>
        <td>1.19</td>
        <td>1.48</td>
    </tr>
    <tr>
        <td>ERD</td>
        <td>1.06</td>
        <td>1.17</td>
        <td>1.19</td>
        <td>1.24</td>
        <td>1.33</td>
        <td>1.41</td>
        <td>1.51</td>
        <td>1.79</td>
    </tr>
    <tr>
        <td>LSTM-3LR</td>
        <td>0.97</td>
        <td>1.07</td>
        <td>1.18</td>
        <td>1.25</td>
        <td>1.37</td>
        <td>1.45</td>
        <td>1.55</td>
        <td>1.79</td>
    </tr>
    <tr>
        <td>SRNN</td>
        <td>0.673</td>
        <td>0.93</td>
        <td>1.02</td>
        <td>1.16</td>
        <td>1.36</td>
        <td>1.44</td>
        <td>1.57</td>
        <td>1.9</td>
    </tr>
    <tr>
        <td>Res-GRU</td>
        <td>0.48</td>
        <td>0.69</td>
        <td>0.9</td>
        <td>1.03</td>
        <td>1.15</td>
        <td>1.23</td>
        <td>1.37</td>
        <td>1.7</td>
    </tr>
    <tr>
        <td>Zero-velocity</td>
        <td>0.39</td>
        <td>0.59</td>
        <td>0.79</td>
        <td>0.89</td>
        <td>1.02</td>
        <td>1.08</td>
        <td>1.22</td>
        <td>1.5</td>
    </tr>
    <tr>
        <td>MHU</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
        <td>-</td>
    </tr>
    <tr>
        <td>HMR</td>
        <td>0.41</td>
        <td>0.6</td>
        <td>0.82</td>
        <td>0.91</td>
        <td>1.04</td>
        <td>1.1</td>
        <td>1.26</td>
        <td>1.57</td>
    </tr>
</table>