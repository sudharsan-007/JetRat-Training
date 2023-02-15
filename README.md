# Jetrat Training Code - Model Training code for JetRat for local training
By [Sudharsan Ananth](https://sudharsanananth.wixsite.com/sudharsan) 

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-this-project">About this Project</a></li>
    <li><a href="#dependencies">Dependencies</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
    <li><a href="#run-the-code">How to run</a></li>
    <li><a href="#license">License</a></li>
  </ol>
</details>


## About this Project 

This is a repository containing the code for Jetrat Training. [JetRat](https://github.com/sudharsan-007/JetRat) is a self-driving car, based on [Nvidia's model architecture](https://images.nvidia.com/content/tegra/automotive/images/2016/solutions/pdf/end-to-end-dl-using-px.pdf). Additionally this code can be used to train data collected from [udacity simulator](https://github.com/udacity/self-driving-car-sim).

Training of the model can be done using this directory. Training code has been tested in Mac and Windows PC. 


### Short Preview of Jetrat (enjoy). 


https://user-images.githubusercontent.com/55453134/218347405-dee79ea0-1b13-40db-bf95-1e4a540c3db0.mov

#### [Watch-full-video-on-youtube](https://youtu.be/gaRUw0A2xp0)


## Dependencies 

This project is built with the below given major frameworks and libraries. The code is primarily based on python. 

* [Python](https://www.python.org/) 
* [pytorch](https://pytorch.org/)
* [matplotlib](https://matplotlib.org/) 
* [pandas](https://pandas.pydata.org) 
* [openCV](https://docs.opencv.org/4.x/d6/d00/tutorial_py_root.html) 
* Optional - [Weights & Biases](https://wandb.ai/site)

## Prerequisites

Collect data from using JetRat and import it as zip file using the commands below.

* zip file for transfer (in Jetson)
  ```sh
  zip -r zipfile.zip directory
  ```
* Transfer into USB drive or use VS code remote extension.
* Import into mac or windows machine for training and paste to this code directory.

## Run the code

Simply clone the repo cd into the right directory and run 'main.py' using the below commands. Step-by-Step instructions given below. 

1. Clone the repository using 
   ```sh
   git clone https://github.com/sudharsan-007/JetRat-Training.git
   ```

2. cd into the directory RL-DQN-Snake-Game
   ```sh
   cd jetrat
   ```

3. Import the data (see prerequisite)
   

4. Check the code main_training and point to right data directory. 
   ```sh
   realData = JetcarDataset("data_dir/data.csv", "data_dir/img/", transform=transforms)
   ```


5. Install pyTorch. Use pip if conda doesn't work. 
    ```sh 
    # https://pytorch.org/get-started/locally/
    conda install pytorch torchvision torchaudio cpuonly -c pytorch
    ```

6. Install Dependencies
   ```sh
   pip install matplotlib opencv-python pandas
   ```

7. Run the Script `main_training.ipynb` to train on data collected from JetRat. 
   ```sh 
   jupyter-notebook main_training.ipynb`
   ```

8. Optional - Run `sim_training.ipynb` to train model on data collected from simulator  
    ```sh 
    jupyter-notebook main.ipynb
    ```

9.  Optional - Run `sweep_test.ipynb` to generate accuracy and loss for all parameters. This uses [Weights & Biases](https://wandb.ai/site). 
    ```sh
    jupyter-notebook sweep_test.ipynb`
    ```


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>
