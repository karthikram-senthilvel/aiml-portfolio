# Understanding Neural Networks

This artifact is a visual presentation that defines and illustrates the core components of a neural network, built using TensorFlow Playground as a hands-on training environment.

## Objective

To solidify understanding of neural network architecture by creating a visual slide deck that explains each component — layers, neurons, weights, activation functions, loss functions, and optimization algorithms — with real observations from a live training run.

## Process

To create this artifact, I followed these steps:

1. Configured and trained a model in TensorFlow Playground (circle dataset, 4→2 hidden layers, tanh activation, learning rate 0.03, batch size 10).
2. Recorded observations from the training run — boundary shape changes, loss curve behavior, and the effect of hyperparameter choices.
3. Designed an 8-slide visual deck defining each neural network component with diagrams, formulas, and personal observations.
4. Wrote a reflection connecting the hands-on experience to broader AI/ML concepts.

## Tools and Technologies Used

* **TensorFlow Playground:** The interactive environment used to train and observe the neural network in real time.
* **PptxGenJS:** Used to programmatically generate the polished visual presentation.
* **GitHub Pages (Jekyll):** Platform hosting this portfolio artifact.

## Reflection

Building this artifact pushed me past a purely conceptual grasp of neural networks. The most striking moment was switching activation functions — with a linear activation, even two hidden layers could only produce a flat boundary. The instant I switched to Tanh, the boundary bent into a closed curve and loss dropped from ~0.51 to ~0.003.

Learning rate behavior was the second key insight. At 0.03 the loss descended smoothly; cranking it higher made the curve oscillate visibly. Seeing gradient descent as a literal "step size" on a live chart connected math to intuition in a way no equation had.

From a professional standpoint, this reinforced something I lean on in supply chain analytics: visualization isn't decoration, it's a diagnostic tool. Creating this deck forced me to translate six abstract components into a visual story a non-specialist could follow — a skill I carry directly into AI/ML client conversations.

## Presentation

[Download Slide Deck](./assets/p7Understanding_Neural_Networks.pptx)
