# FYP-Intelligent-Algorithms-for-DNA-Detection

This repository contains the code for my Final Year Project at Imperial College London on Deep Learning Algorithms for DNA Sequence Detection by Loop-Mediated Isothermal Amplification (LAMP).

## Abstract

Loop-Mediated Isothermal Amplification (LAMP) is a widely used technique for amplifying and detecting DNA sequences. It involves plotting the amplification curve of fluorescence intensity against time cycles, allowing the identification of an amplification reaction, which indicates the presence of the target DNA sequence. However, the application of LAMP for testing multiple DNA primers in a single sample, known as "multiplex LAMP," poses a significant challenge due to difficulties in distinguishing among different amplification reactions. To overcome this limitation, Malpartida-Cardenas et al. proposed a multiplex LAMP technique integrated with amplification curve analysis, employing a machine learning model to automatically classify each curve to its corresponding target DNA. This project aims to enhance this approach by integrating a deep learning Transformer-based model, with the goal of improving overall performance. Additionally, the melting curve, which represents the change in fluorescence intensity against temperature after the amplification reaction, was explored as an alternative using similar deep learning techniques. In future investigations, training the developed framework with transfer learning could be explored to enhance the model’s performance and adaptability.

## Code Structure

The code is organized into three sections:

1. **Data**: This section contains the data visualization, pre-processing, and feature extraction steps.

2. **Amplification Curve**: Here, you can find the implementation and testing of baseline models and Transformer models for amplification curve analysis.

3. **Melt Curve**: This section includes the implementation and testing of baseline models and Transformer models for melt curve analysis.

## Dataset

The dataset used in this project is a private dataset, and access to it is restricted. If you require access to the dataset, please contact me directly.

## Installation

The code is written in a Google Colab environment, and certain adjustements may be necessary to run this code in your own enviroment.

## Results

Promising results were given and reported on my paper.
