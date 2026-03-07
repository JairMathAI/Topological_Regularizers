## Geometric and Topological Regularization for Bioimage Segmentation

This project is detailed in the following [paper](https://)

<span style="color:red;"><b>Important Note:</b></span><br>

We also include the TI_loss this is not part of our proposal but we use it for comparation proposes you can find the info for their original developers [here](https://github.com/TopoXLab/TopoInteraction)

## Installation

Before starting, we recommend [creating a new conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands) or a [virtual environment](https://docs.python.org/3/library/venv.html) with **Python 3.10+**.

```bash
conda create -y -n topo_reg -c conda-forge python=3.11
conda activate topo_reg
```

This project is implemented within our [Im2Im Transformation](https://github.com/MMV-Lab/mmv_im2im/tree/main) framework. To install it, follow the instructions in the corresponding repository:

```bash
git clone https://github.com/MMV-Lab/mmv_im2im.git
cd mmv_im2im
pip install -e .[all]
```

Run 

```bash
pip install -r requirements.txt
``` 

## Regularizator Implementation

If you want to access the implementation of the regularizers for improvements or adaptation to different base loss functions or architectures, you can find the code within the [Im2Im Transformation](https://github.com/MMV-Lab/mmv_im2im/tree/main) project in the [utils folder](https://github.com/MMV-Lab/mmv_im2im/tree/main/mmv_im2im/utils) folder.

With the project installed, you can now train and run inference with the models.

## Trainig

For training, use the provided [YAML templates](docs/yaml_configurations). These files contain clear descriptions of the parameters and training options. Simply set your values, save your configuration, and run:

`run_im2im --config /path/to/your_train_config.yaml`

For more detailed info related to training, please refer to the documentation in our [Im2Im Transformation](https://github.com/MMV-Lab/mmv_im2im/tree/main) repo.

## Inference

We provide an [inference](inference.ipynb) Jupyter notebook to facilitate predictions. It works whether you want to make a prediction with your trained model or manage cases where you have multiple trained versions of the same model and want to run inference over the same dataset.

To use it, run Jupyter Lab, define your model in the provided [YAML templates](docs/yaml_configurations), and follow the instructions in the notebook. 

If you prefer to manually set the full YAML options and run via the command line, follow the inference instructions in our [Im2Im Transformation](https://github.com/MMV-Lab/mmv_im2im/tree/main) repo.

## Evaluation

We provide a [model evaluation](model_evaluation.ipynb) Jupyter notebook that allows you to extract information about model predictions and compare multiple training runs for a single model. 

Simply run the notebook and follow the instructions.

## Some results of the use of our regularizator terms 

<img src="docs/imgs/summ.png" width="800"/>