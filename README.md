# Deploying a Tensorflow Model with Flask

## Installation 

* install miniconda
* create a new environment with flask, tensorflow, and pillow :  

```
conda create -n dlflask python=3.7 tensorflow flask pillow
conda activate dlflask
```

At the moment, later versions of python lead to incompatibilities 
between tensorflow and flask

* install flast-restful with pip 
(since this package is not available in conda) : 

```
pip install flask-restful
```

## Predict a cat

```
python predict_resnet50.py capuchon.jpg
```

Of course, you can try with a picture of yours.

## Flask hello world

Just a very short example of how to use Flask-RESTful.

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

## Predicting image categories with a REST API

```
curl localhost:5000/image -F file=@capuchon.jpg
```

Gives : 

```
{
    "top_categories": [
        [
            "tiger_cat",
            0.5858142375946045
        ],
        [
            "Egyptian_cat",
            0.21068987250328064
        ],
        [
            "tabby",
            0.14554421603679657
        ],
        [
            "pillow",
            0.008319859392940998
        ],
        [
            "lynx",
            0.006789662875235081
        ]
    ]
}
```