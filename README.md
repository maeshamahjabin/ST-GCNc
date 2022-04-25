# ST-GCNc
ST-GCNc

**Abstract** <br />
Human Action Recognition (HAR) is the task of identifying actions performed by humans in real time. HAR plays a crucial role in human-to-computer interactions enabling it to make novel Human-to-Computer Interaction (HCI) models.This paper proposes and verifies the enhancement of previously established ST-GCN model by enriching the message passing mechanism of Spatial Graph Convolutional Neural Network by incorporating more information about the nodes in the graph representation of the skeletons. It introduces a property called the clustering coefficients - the degree of aggregation of the nodes in the graph - into the graph-level update equations, which allows the model to capture richer information at each iteration. This enhancement is validated using the NTU-RGB+D dataset. The project findings effectively verified the work done in paper [1] and gave promising results for the proposed design improvements. The initial simulation results of the ST-GCNc model showed ~3% improvement in cross-view dataset and ~1.6% improvement in cross-sub dataset. With the modification of clustering coefficients, the ST-GCNc model continued to give positive results. Furthermore, supplementary evaluation of the project code was performed by taking into account activation layer, which all together presents notable increase in accuracy of the suggested HAR model and demonstrates state-of-the-art performance.


**Acknowledgements** <br />
Thanks for the framework provided by 'yysijie/st-gcn', which is source code of the published work ST-GCN in AAAI-2018. The github repo is https://github.com/yysijie/st-gcn. The framework has been borrowed and refactored.

**References** <br />
1. Yan, S., Xiong, Y., & Lin, D. (2018, April). Spatial temporal graph convolutional networks for skeleton-based action recognition. In Thirty-second AAAI conference on artificial intelligence.
