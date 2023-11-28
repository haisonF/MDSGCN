# **MDSGCN: A signed graph convolution algorithm for predicting multiple types of mutation-drug association through node labeling** 
Cancer constitutes a significant global public health challenge, resulting in millions of fatalities annually. Gene mutations are pivotal in initiating and advancing cancer, disrupting regular cellular growth and differentiation mechanisms, thereby fostering tumor development. Consequently, comprehending the intricacies of cancer mutations and their interplay with pharmaceuticals is imperative for cancer prevention, diagnosis, and treatment. Despite drug therapy being a cornerstone in cancer treatment, prognosticating and assessing multiple types of mutation-drug association remains a laborious and costly work. To address this problem, we develop a novel deep learning model grounded in signed graph neural network (MDSGCN) to predict multiple types of mutation-drug association. We established mutation-drug association as a signed bipartite network, comprising mutation nodes, drug nodes and two edge types including sensitive or resistant of mutations in drugs. MDSGCN extracts the subgraphs from the mutation-drug pairs in the signed bipartite network, utilizing a label algorithm to learn subgraph structural features. Furthermore, MDSGCN integrates biological features (i.e. mutation-mutation similarity and drug-drug similarity) as the auxiliary information with the subgraph structural features to construct the prediction model. Experiments results demonstrated that our model consistently outperforms the state-of-the-art methods, revealing the effectiveness of MDSGCN in predicting the multiple types of mutation-drug association. Additionally, the case study shows that MDSGCN can discover novel mutation-drug association and the association type. Comprehensive result analysis could offer valuable information for personalized treatment in precision oncology and would make invaluable insights for the advancement and therapeutic application of cancer drugs.





![workflow](E:\MDSGCN\workflow.png)

​    **The workflow of MDSGCN**

## Run

```shell
python main.py -i ./data/m_d.csv -m ./data/m_m.csv -d ./data/d_d.csv -e 20 -s 44
```
### Environment Requirement

The code has been tested running under Python 3.8. The required packages are as follows:

- pytorch==2.1.0
- torch-geometric == 2.3.1
- numpy == 1.19.5
- tensorflow == 1.12.0
- pandas==1.14.4
- scipy==1.9.1
- matplotlib==3.5.3
- scikit-learn==0.22.1
- six==1.16.0





