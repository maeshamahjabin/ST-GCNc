# ST-GCNc
ST-GCNc  <br />
 <br /> **Note:** In this project the term "Validation Dataset" refers to the "Test Dataset". There is only Train and Test datasets used for this project; no seperate validation dataset has been used. The unlabelled "Test dataset" = "Validation dataset".  <br /> <br />
**Abstract** <br />
Human Action Recognition (HAR) is the task of identifying actions performed by humans in real time. HAR plays a crucial role in human-to-computer interactions enabling it to make novel Human-to-Computer Interaction (HCI) models.This paper proposes and verifies the enhancement of previously established ST-GCN model by enriching the message passing mechanism of Spatial Graph Convolutional Neural Network by incorporating more information about the nodes in the graph representation of the skeletons. It introduces a property called the clustering coefficients - the degree of aggregation of the nodes in the graph - into the graph-level update equations, which allows the model to capture richer information at each iteration. This enhancement is validated using the NTU-RGB+D dataset. The project findings effectively verified the work done in paper [1] and gave promising results for the proposed design improvements. The simulation results of the ST-GCNc model showed ~3.8% improvement in cross-view dataset and ~1.7% improvement in cross-sub dataset. With the modification of clustering coefficients, the ST-GCNc model continued to give positive results. 


**Acknowledgements** <br />
Thanks for the framework provided by 'yysijie/st-gcn', which is source code of the published work ST-GCN in AAAI-2018. The github repo is https://github.com/yysijie/st-gcn. This project works with the original code and refactors it.

**References** <br />
1. Yan, S., Xiong, Y., & Lin, D. (2018, April). Spatial temporal graph convolutional networks for skeleton-based action recognition. In Thirty-second AAAI conference on artificial intelligence. <br /> <br />

**Install** <br />
git clone https://github.com/maeshamahjabin/ST-GCNc.git; cd st-gcn cd torchlight; python setup.py install; cd ..

**Data Preparation** <br />
Download Raw 3D skeletal data from: https://rose1.ntu.edu.sg/dataset/actionRecognition/ and allocate the dataset into ”data” folder and process data with: python data/ntu_gendata.py  <br />  <br />
**Training** <br />
For training a new model run:  <br />
python main.py recognition -c config/st_gcn/dataset /train.yaml --batch size 16 --device 0 --test batch size 16  <br />  <br />
**Testing**  <br />
To test a new trained model, run the command:  <br />
python main.py recognition -c config/st_gcn/dataset /test.yaml -- weights path to model weights  <br />  <br />
To test with pre-trained models (from this dissertation) run the command:  <br />
python main.py recognition -c config/st_gcn/dataset/test.yaml --weights work dir/recognition/dataset /ST_GCN/epoch60_model.pt --batch size 16 --device 0 --test batch size 16  <br />  <br />
Note: dataset needs to be either ntu-xview or ntu-xsub.
