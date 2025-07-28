# ml-graphy

A simple and elegant Python package for visualizing machine learning training metrics. `ml-graphy` automatically detects training and validation data to generate clean, publication-ready plots with just one line of code.

## Key Features

- **Automatic Metric Detection**: Intelligently finds `loss`, `accuracy`, `val_loss`, and `val_accuracy` in your model's history.
- **Publication-Ready Plots**: Creates beautiful, clean plots using Seaborn styling.
- **Simple API**: Generate insightful visualizations with a single function call.
- **Training Summary**: Prints a concise summary of final training and validation metrics.

## Installation

Install `ml-graphy` directly from PyPI:

```bash
pip install ml-graphy
```

This will automatically install the required dependencies: `matplotlib` and `seaborn`.

## Quick Start

Using `ml-graphy` is straightforward. Just import the `plot_metrics` function and pass it your trained model object that contains a `history` attribute.

```python
from graphy.plotting import plot_metrics

mod = model.fit(x = train_sample, y = train_label, epochs=100, validation_split=0.2, batch_size=5, shuffle=True, verbose=0)

plot_metrics(mod)
```

This will generate and display side-by-side plots for loss and accuracy.

## What's Next?

The current version of `ml-graphy` focuses on simplicity and core functionality. Future releases will introduce more advanced features to provide greater flexibility and insight into your model's performance. We are actively working on expanding the library's capabilities to support a wider range of visualization needs.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
