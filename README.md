# Aurora Weather prediction

This notebook [Version-1](https://github.com/kutt27/era5-weather-prediction/blob/main/Notebook/version1.ipynb) would crash on setting up with google colab. Unchunked ERA5 pressure levels across 13+ levels at $0.25^\circ$ resolution exceed standard system RAM when loaded directly into NumPy arrays. Full global rollout on $0.25^\circ$ grids ($721 \times 1440$ spatial resolution) demands heavy intermediate activation memory during Swin Transformer attention layers.

Two options moving forward:
- Run the lower resolution 1. 
- Optimize memory in the 0.25 pipeline.

Options avoiding:
- Hugging face own space. Reason: It will work. For anyone reading this can refer to [Hugging Face Space](https://huggingface.co/spaces/hugging-science/ai-weather-models-with-earthmover-data)
