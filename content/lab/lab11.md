---
title: "Lab11"
author: "Wonjun Seo"
summary: "Multi-layer perceptron and Pytorch"
---
## MLP
- <a href="/files/mlp_notes.pdf" download="mlp_notes.pdf">Notes</a>
- <a href="/files/numpy_mlp.ipynb" download="numpy_mlp.ipynb">numpy_MLP</a>

## PyTorch

>For those who had issues with installing `torch`, run the following on terminal to install `torch` properly.
>```bash
>uv add "torch<2.3"
>```

- <a href="/files/pytorch_basics.ipynb" download="pytorch_basics.ipynb">pytorch_basics</a>

### Exercise

Build your own neural network to predict `y` from `X`. You may use Codex to write the code. Use the prompt template below.

<a href="/files/prompt_template.md" download="prompt_template.md">**prompt_template**</a>

**Train set**
- <a href="/files/X_train.csv" download="X_train.csv">X_train</a>
- <a href="/files/y_train.csv" download="y_train.csv">y_train</a>

**Test set**

Will be provided at the end of lab session. Your model will be evaluated on test data. Whoever achieves the lowest test loss will receive a special prize on Friday!

> All variables are already properly scaled. No need to do further scaling.

- <a href="/files/X_test.csv" download="X_test.csv">X_test</a>
- <a href="/files/y_test.csv" download="y_test.csv">y_test</a>

Locate the above files at the same directory of your `ipynb` file and then run the following
```python
import torch.nn as nn

X_test, y_test = pd.read_csv("X_test.csv", header=None), pd.read_csv("y_test.csv", header=None)
X_test, y_test = torch.tensor(X_test.values, dtype=torch.float32), torch.tensor(y_test.values, dtype=torch.float32)

model.load_state_dict(best_model_state)
model.eval()

with torch.no_grad(): 
    y_test_pred = model(X_test)

test_loss = nn.MSELoss()(y_test_pred, y_test)

print(f'Test loss: {test_loss: .4f}')
```


