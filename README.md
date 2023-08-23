# LittleAdversary

LittleAdversary is an adversarial machine learning library made to aid
research into adversarial attacks and defences, with a primary focus on
one-shot defences. The library features pre-trained, small neural
networks replicating security-critical tasks that can be attacked with
adversarial examples and defended, either by traditional adversarial
training or by our novel siamese verification networks. This library was
released as part of the paper \'Siamese Neural Networks for One-shot
Adversarial Robustness\' and as such, it contains Jupyter notebooks
detailing how to use siamese neural networks to defend against adversarial
attacks without requiring a large dataset of adversarial examples. The 
library also contains modified versions of popular adversarial attacks, 
altered to attack siamese neural networks.

## Author

Harry Collins

## Installation

Install JupyterLabs with the following pip command: pip install
jupyterlab Then, in the LittleAdversary directory, run pip install -r
requirements.txt to install the remaining required libraries.

To run the Jupyter notebooks, you must run Jupyter on your device after installing it, and then open
the notebooks from your localhosted Jupyter instance.

https://www.dataquest.io/blog/jupyter-notebook-tutorial/
This site has a good guide on how to run Jupyter notebooks if more help is needed.

## Usage

There are four modules:

#### Notebooks

This module contains all of the code. Notebooks starting with \'utils\'
simply provide utilities to help run the main notebooks, and can be used
to streamline the process of building new neural network models and
adversarially training them.

Notebooks starting with \'Building\' show how to build and train each of
the small, undefended neural network models in the library. All models
are saved to the models module.

The \'Adversarial One-shot Training (Siamese Verification Networks and
Traditional Adversarial Training)\' guides the user through how to use
one-shot learning to create versions of the original models that are
defended against adversarial examples. Several traditionally
adversarially trained models and siamese verification networks are
trained for each of the original undefended models, and they are only
trained with a single adversarial example injected into the dataset. If
the user wishes, they can change this when following along, and increase
the number of injected adversarial examples if they wish. All models are
saved to the models module.

The \'Adversarial Defence Experiment, Evaluation and Results\' notebook
details the running of the experiment from the paper \'Siamese Neural
Networks for One-shot Adversarial Robustness\'. It allows the user to
test their neural network models\' robustness against adversarial
examples and to compare different defences.

The \'siamese_attack_variants\' notebook contains modified versions of
adversarial attacks from CleverHans
https://github.com/cleverhans-lab/cleverhans, altered to attack siamese
neural networks which take pairs of inputs rather than single inputs.
Therefore, these variants generate adversarial pairs of inputs e.g. face
images.

#### Models

This module is where all the models and model weights trained for the
library are stored.

#### Data

This module stores the datasets used to train the models.

#### Graphs

Here, we store visualisations of our results, training histories, and
some examples of adversarial data.

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

## License

\[MIT\](https://choosealicense.com/licenses/mit/)
