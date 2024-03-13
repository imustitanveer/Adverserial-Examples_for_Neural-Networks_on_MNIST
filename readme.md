# Adversarial Examples for Neural Networks

This project explores adversarial attacks on neural networks using different methods. The proposed method, "Projected Gradient Descent Method," is compared against the traditional "Fast Sign Gradient Method." The Projected Gradient Descent method iteratively optimizes the input image to maximize the model's loss function, ensuring the modified image remains within a predetermined distance from the original input (ϵ). 

## Methodology

The `PGD_Attack` function is used to iteratively perturb the input image `x` towards maximizing the loss function, while ensuring the modified image stays within the ϵ boundary. The `fgsm_attack` function implements the Fast Gradient Sign Method for comparison. 

## Results

The experimental results show the accuracy of adversarial images as a function of Epsilon. The Projected Gradient Descent method consistently outperforms the Fast Sign Gradient Method, reaching lower accuracy in all tests and achieving 0 accuracy before FSGM. However, PGD is computationally expensive compared to FSGM. 

## Experimental Setup

The `evaluate_on_adversarial_fgsm` and `evaluate_on_adversarial_pgd` functions evaluate the accuracy on adversarial examples using FGSM and PGD attacks, respectively. The accuracy is calculated on adversarial images without considering error bars or confidence levels.

## Usage

The project includes the implementation of the adversarial attack methods and evaluation functions. To use the project, clone the repository and run the provided code. 

## Experimental Results Images

The folder `results_images` contains images of the original and adversarial examples generated using the FGSM and PGD methods. 

