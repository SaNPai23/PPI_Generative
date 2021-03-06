# PPI_Generative

## This is the readme file that contains the guidelines and information about the compilation of the code of the following paper

**Paper Name:-** [Protein-protein Interaction based Generative Model for Improving Gene Clustering](https://www.nature.com/articles/s41598-020-57437-5)

- **Authors:** Pratik Dutta<sup>1</sup>, Sanket Pai<sup>2</sup>, Aviral Kumar<sup>2</sup> and Sriparna Saha<sup>1</sup>
- **Affiliation:** <sup>1</sup>Department of Computer Science and Engineering, IIT Patna, India, <sup>2</sup>Depatment of Chemical Science and Technology, IIT Patna, India
- **Accepted:(20/12/2019)** [Scientific Reports-Nature](https://www.nature.com/srep/)

If you consider this work as useful, please cite it as 
```bash
@article{pratik2020protein,
  title={A Protein Interaction Information-based Generative Model for Enhancing Gene Clustering},
  author={Pratik, Dutta and Sriparna, Saha and Sanket, Pai and Aviral, Kumar},
  journal={Scientific Reports (Nature Publisher Group)},
  volume={10},
  number={1},
  year={2020},
  publisher={Nature Publishing Group}
}
```


 This repository contains code a **protein-protein interaction-based generative model** that can efficiently perform a **gene clustering**. In this work, **protein-protein interaction(PPI)** information is used as a latent variable of the **generative model**. The proposed generative model is fusion of protein interaction with [Snorkel](https://github.com/HazyResearch/snorkel). 
 ![flowchart_pic](https://user-images.githubusercontent.com/29531232/69358402-c9eecc80-0cac-11ea-923f-c003c0ae27b0.png)

 
 ## Getting Started 
 These instructions will allow you to emulate the results obtained from the code for development and testing purposes.
 ### Prerequisites
* **[Python 2.7+](https://www.python.org/downloads/release/python-2713/)** {*For MOO-based clustering.*}
* **[Python 3.6](https://www.python.org/downloads/)** {*For developing generative model*}
* **[sklearn](https://scikit-learn.org/stable/install.html)**
* **[matplotlib 2.0+](https://matplotlib.org/users/installing.html)**
* **[mpl_toolkits](https://matplotlib.org/2.0.2/mpl_toolkits/index.html)**
* **[numpy 1.10+](https://pypi.org/project/numpy/)**
* **[Snorkel](https://github.com/HazyResearch/snorkel)**

### Setup
All our code is implemented in Python. The installation instructions are as follows:                                                       
> git clone                                                                                                     
> python get-pip.py                                                                                                                  
> pip install numpy                                                                                                                     
> pip install matplotlib                                                                                                                 
> pip install numpy scipy scikit-learn                                                                                                   

If the above doesn't work try upgrading the setup tools as follows -                                                                   
> pip install --upgrade setuptools

**NOTE:** To install Snorkel follow the given steps or refer **[here](https://github.com/HazyResearch/snorkel)** .
This section is meant to help setup Snorkel on your systems. For more detailed instructions see the **[Installation section](https://github.com/HazyResearch/snorkel#installation)**. These instructions assume that you already have conda installed.
First, download and extract a copy of the Snorkel directory from a **[GitHub release](https://github.com/HazyResearch/snorkel/releases)** (version 0.7.0 or greater). Then navigate to the root of the snorkel directory in a terminal and run the following:
> install the environment                                                                                                               
> conda env create --file=environment.yml                                                                                               
> activate the environment                                                                                                              
> source activate snorkel                                                                                                               
> install snorkel in the environment                                                                                                     
> pip install


## Description
### 1. MOO-based Clustering
The details procedure for running the MOO-based clustering is described in the our [GitHub repository](https://github.com/sduttap16/DeepEnsm). 

### 2. Generative Model
The proposed generative model utilizes protein interaction information as the weighted factor for each solution. This folder contains additional files that helps to integrate the protein interaction information with the generative model. The `generative model` is obtained from the [Snorkel](https://github.com/HazyResearch/snorkel). To run the code, please activate [Snorkel](https://github.com/HazyResearch/snorkel) environment. Then download the following files and store in the main folder

* `panther.py` This file is used to generate additional labels from GO-based solutions which is incorporated along with MOO-based solutions in order to increase the biological significance.

* `ppi_in.py` TThis file is used to process the data obtained from the protein - protein Interaction database which is used to generate weights which represent the accuracy of the weak supervision sources.

* `PPI_gen_model.ipynb`  Protein interaction based modified implementation of the generative model. This modified generative model takes both MOO-based clustering and GO-based solutions along with the protein interaction information to generate final labels.


## Authors
- [Pratik Dutta](http://www.iitp.ac.in/~pratik.pcs16/) (Ph.D, Indian Institute of Technology Patna)
- Sanket Pai (B.Tech, Indian Institute of Technology Patna)
- Aviral Kumar (B.Tech Indian Institute of Technology Patna)
- [Dr. Sriparna Saha](https://www.iitp.ac.in/~sriparna/)(Associate professor, Indian Institute of Technology Patna)

## Contribution
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. Also you can contact to the corresponding author Pratik Dutta (pratik.pcs16@iitp.ac.in )
