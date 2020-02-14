---
title: Microsoft Azure
layout: content
image: water-paints-1057934-pxh.jpg
---
NOTE: right now, most of this is directly copied from Microsoft's documentation or ad copy

Chris Lauren, Principle Program Manager Lead
(@clauren42)
Azure Machine Learning Platform


## Azure Machine Learning designer (preview)
- Available only in Enterprise edition workspaces
- Use the designer to prep data, train, test, deploy, manage, and track machine learning models without writing any code. There is no programming required, you visually connect datasets and modules to construct your model. T
- Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try Azure Machine Learning designer (preview), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
- Develop machine learning training scripts in Python or with the visual designer, Create and configure a compute target, then Submit the scripts to the configured compute target to run in that environment
- Deploy - Develop a scoring script that uses the model and Deploy the model as a web service in Azure, or to an IoT Edge device.

- Meanwhile, Azure Machine Learning provides both a web interface called the designer (preview) and several SDKs and CLI to quickly prep data, train and deploy machine learning models. With Azure Machine Learning you get scale, multiple framework support, advanced ML capabilities like automated machine learning and pipeline support.
- Azure Machine Learning designer provides a similar drag-and-drop experience to Studio (classic). However, unlike the proprietary compute platform of Studio (classic), the designer uses your own compute resources, is scalable, and is fully integrated into Azure Machine Learning.

## Random Notes About Azure Machine Learning
- Estimators make it easy to train models using popular ML frameworks. If you're using Scikit-learn, PyTorch, TensorFlow, or Chainer, you should consider using an estimator for training.
- CLI: The machine learning CLI provides commands for common tasks with Azure Machine Learning, and is often used for scripting and automating tasks. For example, once you've created a training script or pipeline, you might use the CLI to start a training run on a schedule or when the data files used for training are updated.


## About Machine Learning Studio (classic)
- Machine Learning Studio (classic) is a collaborative, drag-and-drop visual workspace where you can build, test, and deploy machine learning solutions without needing to write code. It uses prebuilt and preconfigured machine learning algorithms and data-handling modules as well as a proprietary compute platform.
