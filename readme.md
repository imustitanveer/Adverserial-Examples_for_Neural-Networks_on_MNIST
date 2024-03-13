# Adversarial Examples for Neural Networks

This project explores adversarial attacks on neural networks using different methods. The proposed method, "Projected Gradient Descent Method," is compared against the traditional "Fast Sign Gradient Method." The Projected Gradient Descent method iteratively optimizes the input image to maximize the model's loss function, ensuring the modified image remains within a predetermined distance from the original input (ϵ). 

## Methodology

The `PGD_Attack` function is used to iteratively perturb the input image `x` towards maximizing the loss function, while ensuring the modified image stays within the ϵ boundary. The `fgsm_attack` function implements the Fast Gradient Sign Method for comparison. 

## Results

The table below shows the accuracy of the adversarial image as a function of Epsilon for both the Fast Gradient Sign Method and the Projected Gradient Descent method:

| Epsilon | Fast Gradient Sign Method | Projected Gradient Descent |
|---------|---------------------------|-----------------------------|
| 0.05    | 0.335                     | 0.296                       |
| 0.1     | 0.014                     | 0.007                       |
| 0.15    | 0.002                     | 0                           |
| 0.2     | 0                         | 0                           |

The tests directly calculated the accuracy of the model on adversarial images without making use of error bars and confidence levels for both methods.

## Experimental Setup

The `evaluate_on_adversarial_fgsm` and `evaluate_on_adversarial_pgd` functions evaluate the accuracy on adversarial examples using FGSM and PGD attacks, respectively. The accuracy is calculated on adversarial images without considering error bars or confidence levels.

## Usage

The project includes the implementation of the adversarial attack methods and evaluation functions. To use the project, clone the repository and run the provided code. 

## Experimental Results Images

The folder `results_images` contains images of the original and adversarial examples generated using the FGSM and PGD methods. 

