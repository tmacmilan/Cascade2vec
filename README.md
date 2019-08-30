# Cascade Preidction
This is the link for codes and data used in the paper <Cascade2vec: Learning Dynamic Cascade Representation by Recurrent Graph Neural Networks.>. The paper is still under review. The codes will be fully released as soon as possible after the paper is published. The paper targets on cascade prediction, one of the fundemental problems in information diffusion.



# Cascade Example
What is a cascade?
A cascade is also called information diffusion/dissemination networks. It records how information propagates between people. Examples of full cascades can be seen in the links https://github.com/zhenhuascut/diffusion-data.

# Graph Perception Network

In the paper, we propose a new graph neural network called graph perception network (GPN), which achieves the state-of-the-art performance in graph classification tasks. 

The results between the GPN and baselines are as follows:

for example:
```
run the main.py --dataset 'MUTAG'
```
The datasets can be chosen from ['COLLAB', 'NCI1', 'MUTAG', 'PTC', 'PROTEINS', 'IMDB-M', 'IMDB']

The experiments results on these datasets are as follows:
## MUTAG:
The accuracy of each folder:

{0: 0.85, 1: 0.9, 2: 0.95, 3: 0.9473684210526315, 4: 0.8947368421052632, 5: 1.0, 6: 0.9444444444444444, 7: 0.9444444444444444, 8: 1.0, 9: 0.9444444444444444}

mean:0.9375438596491229
std:0.04370581208082047

## PTC:

The accuracy of each folder:

{0: 0.6944444444444444, 1: 0.7222222222222222, 2: 0.7352941176470589, 3: 0.6470588235294118, 4: 0.6470588235294118, 5: 0.6764705882352942, 6: 0.6764705882352942, 7: 0.5882352941176471, 8: 0.6764705882352942, 9: 0.6176470588235294}

mean: 0.6681372549019609
std: 0.04261198567800631

## IMDB-M:

The accuracy of each folder:

{0: 0.5466666666666666, 1: 0.5333333333333333, 2: 0.5533333333333333, 3: 0.5066666666666667, 4: 0.5133333333333333, 5: 0.5733333333333334, 6: 0.5733333333333334, 7: 0.5, 8: 0.56, 9: 0.54}
mean: 0.5400000000000001
std: 0.025121924908555707

## PROTEINS:

The accuracy of each folder:

{0: 0.7589285714285714, 1: 0.8214285714285714, 2: 0.8125, 3: 0.8018018018018018, 4: 0.8108108108108109, 5: 0.7747747747747747, 6: 0.7477477477477478, 7: 0.7477477477477478, 8: 0.7837837837837838, 9: 0.8198198198198198}

mean:0.787934362934363
std:0.027783661934815667

The results can be vary a little bit.


# Cascade2vec
When we run the cascade2vec in the Microblog network dataset provided by Prof. Shen in DeepHawkes CIKM'17.
Using the following command: 
```
python cascade_dynamic_gnnlstm.py --T 1 --dataset=microblog
```
T=1 represents the observation time is 1 hour.

when T is set to 1 hour, the result looks like this:

<div>0&nbsp;</div><div>average train loss 4.8758</div><div>median train loss 1.3386</div><div>r2score train 0.0107</div><div>average test loss 2.8691</div><div>median test loss 0.9733</div><div>r2score test 0.3917</div><div>1&nbsp;</div><div>average train loss 2.9229</div><div>median train loss 0.8689</div><div>r2score train 0.4069</div><div>average test loss 2.4599</div><div>median test loss 0.8198</div><div>r2score test 0.4784</div><div>2&nbsp;</div><div>average train loss 2.6231</div><div>median train loss 0.7962</div><div>r2score train 0.4678</div><div>average test loss 2.2960</div><div>median test loss 0.7010</div><div>r2score test 0.5045</div><div>3&nbsp;</div><div>average train loss 2.3933</div><div>median train loss 0.7215</div><div>r2score train 0.5080</div><div>average test loss 2.1476</div><div>median test loss 0.6715</div><div>r2score test 0.5282</div><div>4&nbsp;</div><div>average train loss 2.2379</div><div>median train loss 0.6713</div><div>r2score train 0.5322</div><div>average test loss 2.0935</div><div>median test loss 0.6796</div><div>r2score test 0.5402</div><div>5&nbsp;</div><div>average train loss 2.1241</div><div>median train loss 0.6101</div><div>r2score train 0.5545</div><div>average test loss 2.0858</div><div>median test loss 0.7025</div><div>r2score test 0.5418</div><div>6&nbsp;</div><div>average train loss 2.0639</div><div>median train loss 0.5935</div><div>r2score train 0.5642</div><div>average test loss 2.0528</div><div>median test loss 0.6494</div><div>r2score test 0.5491</div><div>7&nbsp;</div><div>average train loss 1.9872</div><div>median train loss 0.5380</div><div>r2score train 0.5774</div><div>average test loss 2.0514</div><div>median test loss 0.6606</div><div>r2score test 0.5328</div><div>8&nbsp;</div><div>average train loss 1.9295</div><div>median train loss 0.5655</div><div>r2score train 0.5899</div><div>average test loss 2.0459</div><div>median test loss 0.6322</div><div>r2score test 0.5508</div><div>9&nbsp;</div><div>average train loss 1.8665</div><div>median train loss 0.5614</div><div>r2score train 0.6016</div><div>average test loss 2.0905</div><div>median test loss 0.6440</div><div>r2score test 0.5407</div><div>10&nbsp;</div><div>average train loss 1.8226</div><div>median train loss 0.5436</div><div>r2score train 0.6109</div><div>average test loss 2.0527</div><div>median test loss 0.6685</div><div>r2score test 0.5490</div><div>11&nbsp;</div><div>average train loss 1.7725</div><div>median train loss 0.5369</div><div>r2score train 0.6202</div><div>average test loss 2.0919</div><div>median test loss 0.6718</div><div>r2score test 0.5404</div><div>12&nbsp;</div><div>average train loss 1.7443</div><div>median train loss 0.5170</div><div>r2score train 0.6238</div><div>average test loss 2.0549</div><div>median test loss 0.6213</div><div>r2score test 0.5485</div><div>13&nbsp;</div><div>average train loss 1.6918</div><div>median train loss 0.4971</div><div>r2score train 0.6338</div><div>average test loss 2.1149</div><div>median test loss 0.6520</div><div>r2score test 0.5353</div><div>14&nbsp;</div><div>average train loss 1.6498</div><div>median train loss 0.5133</div><div>r2score train 0.6502</div><div>average test loss 2.0606</div><div>median test loss 0.6487</div><div>r2score test 0.5472</div><div>15&nbsp;</div><div>average train loss 1.6119</div><div>median train loss 0.4789</div><div>r2score train 0.6571</div><div>average test loss 2.0513</div><div>median test loss 0.6791</div><div>r2score test 0.5493</div><div>16&nbsp;</div><div>average train loss 1.5770</div><div>median train loss 0.4720</div><div>r2score train 0.6645</div><div>average test loss 2.0377</div><div>median test loss 0.6126</div><div>r2score test 0.5438</div><div>17&nbsp;</div><div>average train loss 1.5369</div><div>median train loss 0.4179</div><div>r2score train 0.6730</div><div>average test loss 2.0484</div><div>median test loss 0.6330</div><div>r2score test 0.5235</div><div>18&nbsp;</div><div>average train loss 1.4985</div><div>median train loss 0.4149</div><div>r2score train 0.6790</div><div>average test loss 2.0545</div><div>median test loss 0.5850</div><div>r2score test 0.5568</div><div>19&nbsp;</div><div>average train loss 1.4762</div><div>median train loss 0.4145</div><div>r2score train 0.6768</div><div>average test loss 2.0448</div><div>median test loss 0.5788</div><div>r2score test 0.5667</div><div><br /></div><div>......</div><div><br /></div>



When T is set to 2 hour, the result looks like this:

<div>0</div><div>average train loss 4.6583</div><div>median train loss 1.2830</div><div>r2score train 0.1298</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.4496</div><div>median test loss 0.7771</div><div>r2score test 0.5228</div><div>1</div><div>average train loss 2.3603</div><div>median train loss 0.7230</div><div>r2score train 0.5381</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.3273</div><div>median test loss 0.7151</div><div>r2score test 0.5433</div><div>2</div><div>average train loss 2.2610</div><div>median train loss 0.6689</div><div>r2score train 0.5552</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.2859</div><div>median test loss 0.6834</div><div>r2score test 0.5527</div><div>3</div><div>average train loss 2.2054</div><div>median train loss 0.6440</div><div>r2score train 0.5661</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.2404</div><div>median test loss 0.6598</div><div>r2score test 0.5615</div><div>4</div><div>average train loss 2.1663</div><div>median train loss 0.6297</div><div>r2score train 0.5742</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.1774</div><div>median test loss 0.6207</div><div>r2score test 0.5699</div><div>5</div><div>average train loss 2.1317</div><div>median train loss 0.6138</div><div>r2score train 0.5814</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.1516</div><div>median test loss 0.6173</div><div>r2score test 0.5742</div><div>6</div><div>average train loss 2.1049</div><div>median train loss 0.6027</div><div>r2score train 0.5873</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.1302</div><div>median test loss 0.6084</div><div>r2score test 0.5822</div><div>7</div><div>average train loss 2.0848</div><div>median train loss 0.5953</div><div>r2score train 0.5918</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.1190</div><div>median test loss 0.6123</div><div>r2score test 0.5842</div><div>8</div><div>average train loss 2.0666</div><div>median train loss 0.5868</div><div>r2score train 0.5961</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0947</div><div>median test loss 0.6060</div><div>r2score test 0.5886</div><div>9</div><div>average train loss 2.0496</div><div>median train loss 0.5814</div><div>r2score train 0.5992</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.1081</div><div>median test loss 0.6098</div><div>r2score test 0.5856</div><div>10</div><div>average train loss 2.0330</div><div>median train loss 0.5803</div><div>r2score train 0.6024</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0889</div><div>median test loss 0.5950</div><div>r2score test 0.5897</div><div>11</div><div>average train loss 2.0180</div><div>median train loss 0.5717</div><div>r2score train 0.6056</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0889</div><div>median test loss 0.5929</div><div>r2score test 0.5900</div><div>12</div><div>average train loss 2.0017</div><div>median train loss 0.5692</div><div>r2score train 0.6084</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0705</div><div>median test loss 0.5922</div><div>r2score test 0.5934</div><div>13</div><div>average train loss 1.9868</div><div>median train loss 0.5647</div><div>r2score train 0.6118</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0307</div><div>median test loss 0.5823</div><div>r2score test 0.6030</div><div>14</div><div>average train loss 1.9768</div><div>median train loss 0.5627</div><div>r2score train 0.6136</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0464</div><div>median test loss 0.5795</div><div>r2score test 0.5997</div><div>15</div><div>average train loss 1.9590</div><div>median train loss 0.5601</div><div>r2score train 0.6173</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0402</div><div>median test loss 0.5708</div><div>r2score test 0.5990</div><div>16</div><div>average train loss 1.9472</div><div>median train loss 0.5577</div><div>r2score train 0.6195</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0195</div><div>median test loss 0.5724</div><div>r2score test 0.6044</div><div>17</div><div>average train loss 1.9349</div><div>median train loss 0.5517</div><div>r2score train 0.6215</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0108</div><div>median test loss 0.5603</div><div>r2score test 0.6064</div><div>18</div><div>average train loss 1.9252</div><div>median train loss 0.5526</div><div>r2score train 0.6234</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 1.9995</div><div>median test loss 0.5625</div><div>r2score test 0.6080</div><div>19</div><div>average train loss 1.9112</div><div>median train loss 0.5489</div><div>r2score train 0.6260</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0159</div><div>median test loss 0.5619</div><div>r2score test 0.6034</div><div>20</div><div>average train loss 1.8998</div><div>median train loss 0.5466</div><div>r2score train 0.6284</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 2.0060</div><div>median test loss 0.5544</div><div>r2score test 0.6067</div><div>21</div><div>average train loss 1.8871</div><div>median train loss 0.5437</div><div>r2score train 0.6304</div><div>total test batch: 118.53125&nbsp;</div><div>average test loss 1.9950</div><div>median test loss 0.5546</div><div>r2score test 0.6092</div><div><br /></div><div>......</div><div><br /></div>


Note that the median loss not always decreases with MSE.


When we run the cascade2vec in the APS citation network dataset provided by APS.
Using the following codes:
```
python cascade_dynamic_gnnlstm.py --T 5 --dataset=citation
```
T=5 represents 5 years when the dataset is set to the APS citation network.



# Requirements:
<div>six==1.12.0</div><div>networkx==2.0</div><div>torch==1.1.0</div><div>tensorflow==1.13.1</div><div>numpy==1.16.4</div><div>typing==3.6.2</div><div>scipy==1.2.1</div><div>tqdm==4.32.1</div><div>matplotlib==2.1.0</div><div>Keras==2.2.4</div><div>torch_geometric==1.2.0</div><div>scikit_learn==0.21.3</div>

The experiments are tested on RTX 2080 Ti.

# Acknowledgement:
In addition to the funds that support the study, we are also very grateful to the following researchers.

We thank Prof. Xifeng Yan in UCSB for his help in the research.

We are grateful to Shunfeng Zhou from SenseTime Tech. for helping us implement efficiency graph neural networks on sparse graphs.

We thank Dr. Matthias Fey for providing insights on improving graph neural networks. 

Thanks for Dr. Martin Liu in UCI for his help in algorithm anlaysis.
