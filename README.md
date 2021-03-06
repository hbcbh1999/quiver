# Quiver
Interactive convnet features visualization for Keras


![gzqll3](https://cloud.githubusercontent.com/assets/5866348/20253975/f3d56f14-a9e4-11e6-9693-9873a18df5d3.gif)




**The quiver workflow**

[Video Demo](https://www.youtube.com/watch?edit=vd&v=tgRW3BRi_FA)

1. Build your model in keras

    ```python
    model = Model(...)
    ```
2. Launch the visualization dashboard with 1 line of code

    ```python
    quiver_engine.server.launch(model, input_folder='./imgs')
    ```
3. Explore layer activations on all the different images in your input folder.


## Quickstart

**Installation**

```bash
    pip install quiver_engine
```


**Usage**

Take your keras `model`, launching Quiver is a one-liner.

```python
    from quiver_engine import server
    server.launch(model)
```

This will launch the visualization at `localhost:5000`

**Options**

```python
    server.launch(
        model, # a Keras Model

        # where to store temporary files generatedby quiver (e.g. image files of layers)
        temp_folder='./tmp',

        # a folder where input images are stored
        input_folder='./',

        # the localhost port the dashboard is to be served on
        port=5000
    )
```

## Development

**Building from master**

Check out this repository and run

```bash
python setup.py develop
```

**Building the Client**

```bash
    export QUIVER_URL=localhost:5000 # or whatever you set your port to be
    cd quiverboard
    npm start
```

## Credits
- This is essentially an implementation of some ideas of [deepvis](https://github.com/yosinski/deep-visualization-toolbox) and related works.
- A lot of the pre/pos/de processing code was taken from [here](https://github.com/fchollet/deep-learning-models) and other writings of [fchollet](https://github.com/fchollet).


