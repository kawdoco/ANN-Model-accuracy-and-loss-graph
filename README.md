**#ANN Lab - Susara Thenuwara 179418b**

**##**** Model accuracy and loss graph with apply any initializers**

![](RackMultipart20210925-4-ypzjfh_html_2da6453fb163cd99.png) ![](RackMultipart20210925-4-ypzjfh_html_518b58605a8a04d2.png)

When increasing the epochs error decreased and accuracy increased.

**##**** Weight initialize to zero**

![](RackMultipart20210925-4-ypzjfh_html_b8bceb35bd222435.png) ![](RackMultipart20210925-4-ypzjfh_html_bbd4971f3293bbe8.png)

This is not suitable for this dataset. the first have the same values and symmetric features at the initialization. No variation or different features can learn this is not good procedure and not able to learn faster. All the hidden neurons have the symmetric feature.

**##**** Bias initialization zero**

![](RackMultipart20210925-4-ypzjfh_html_d249656de7d0a258.png) ![](RackMultipart20210925-4-ypzjfh_html_53944f441f15376d.png)

This perfectly work as it increases the accuracy with the number of epochs and error decreased.

**##**** Weight initialize to random normal**

![](RackMultipart20210925-4-ypzjfh_html_f79f3a017e85b461.png) ![](RackMultipart20210925-4-ypzjfh_html_9c519e62e7c92cf.png)

Weights are initialized with normal distribution randomly. Therefore, model work perfect but not perfect like truncated normal bcoz the weight initialization rage are larger. Accuracy is less than truncated normal weight initializing.

**##**** Weight initialize to truncated normal**

We need &#39;W&#39; in circular form as much as possible then lean smoothly and faster. In order to do that What we need to do is W have in same scale but different, truncate the normal distribution to **limited range and initializes** the weights from that range, mean zero, sigma is 0.05. but it will give different accuracy at different experiments.

![](RackMultipart20210925-4-ypzjfh_html_a8b5626082a84910.png) ![](RackMultipart20210925-4-ypzjfh_html_c1eedf3b0d73c0ba.png)

We define the standard deviation 0.05 and this work perfectly. It depends on weight values it initialized. Model accuracy increased over the number of epochs and error decreased. We need to initialize the weight in same range but different.

**##**** He initialization to weights**

![](RackMultipart20210925-4-ypzjfh_html_1fc34fb30b84af29.png) ![](RackMultipart20210925-4-ypzjfh_html_e073c72a6bc1fad7.png)

this also work perfectly rather than going to random truncated normal. Sigma based on the number of neurons in the previous layer. Model accuracy increased over the number of epochs and error decreased. Sigma based on the number of neurons in the previous layer. Variance proportional to the number of neurons in the previous layer. It gives variation of weights as a function of hidden neuron in the previous layer. It gives minimum variance require t for the weight values to learn the features.

**##**** With dropouts**

With dropouts it seems to increase the test accuracy over time. This is because we are dropping the final hidden layer neurons by comparing keep probability and it eventually make the network to generalize well and increase the accuracy.

**##**** L2 Regularization without Dropouts**

By adding L2 regularization it obtained higher accuracy over testing batches, i.e. 0.55. This is because its adding a upper limit to the weight update an keep inside the balancing interval to memorize the features rather than making it to memorize noisy features without keeping a limit

**##**** L2 Regularization with Dropouts**

Although it is expected to have a higher accuracy (atleast than 0.55 with L2 regularization) surprisingly here we got rather a same accuracy as with dropouts. This can be due to the number of neurons per layer and having the less number of layers.
 
