# manager-tool

`manager-tool` is a Python library which makes graphics toolkit with WebGL easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `manager-tool`, clone and install requirements:

```
git clone https://github.com/user/manager-tool
cd manager-tool
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model typograf --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - ChatRecord

```python
from manager-tool import models

model = models.ChatRecord(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| typograf | **78.61** | [Code](#), [Paper](#) |
| ChatRecord | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!


# PR Merge: 2026-08-05 05:04:05

# PR Update: 2026-08-05 05:04:31
