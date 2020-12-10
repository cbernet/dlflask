# Deploying a Tensorflow Model with Flask

## Installation 

* install miniconda
* create a new environment with flask, tensorflow, and pillow :  

```
conda create -n dlflask python=3.7 tensorflow flask pillow
conda activate dlflask
```

At the moment, later versions of python lead to incompatibilities between tensorflow and flask

* install flast-restful with pip (not available in conda) : 

```
pip install flask-restful
```

## Predict a cat

```
python predict_resnet50.py
```

## Flask hello world

Start the app server: 

```
python rest_api_hello.py
```

Send a request:

```
curl localhost:5000/hello
> 
{
    "hello": "world"
}
```

## Predicting image categories 

