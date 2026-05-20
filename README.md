# distilbert-goodreads-genres

This project fine-tunes a DistilBERT model for multi-class genre classification on the Goodreads dataset, classifying book descriptions into 8 different genres (Children, Comics/Graphic, Fantasy/Paranormal, History/Biography, Mystery/Thriller/Crime, Poetry, Romance, and Young Adult). To run this project, install dependencies using `pip install -r requirements.txt`, then open the Jupyter notebook and execute all cells sequentially (ensure you have set `WANDB_API_KEY` and `HF_TOKEN` environment variables for experiment tracking and model deployment). The training was performed on **Kaggle Notebook** with GPU acceleration, and you can view the complete notebook at [https://www.kaggle.com/code/reeteshsingh/distilbert-goodreads-classification](https://www.kaggle.com/code/reeteshsingh/distilbert-goodreads-classification). The trained model is publicly available on Hugging Face at [https://huggingface.co/reeteshsingh/distilbert-goodreads-genres](https://huggingface.co/reeteshsingh/distilbert-goodreads-genres), and all training experiments, metrics, and artifacts can be viewed on the Weights & Biases dashboard at [https://wandb.ai/g25ait2086-iit-jodhpur/huggingface](https://wandb.ai/g25ait2086-iit-jodhpur/huggingface).

## Results

### Final Model Performance
| Metric | Value |
|--------|-------|
| Accuracy | 58.13% |
| F1 Score | 58.73% |
| Precision | 60.44% |
| Recall | 58.13% |
| Loss | 2.607 |

### Training Progress
| Epoch | Training Loss | Validation Loss | Accuracy | F1 Score |
|-------|---------------|-----------------|----------|----------|
| 1 | 1.177 | 2.607 | 58.06% | 58.67% |
| 2 | 0.934 | 2.737 | 59.94% | 60.05% |
| 3 | 0.632 | 2.983 | 59.56% | 59.74% |

### Baseline Comparison
| Model | Accuracy | F1 Score |
|-------|----------|----------|
| Logistic Regression (TF-IDF) | 55.00% | 55.00% |
| DistilBERT (Fine-tuned) | 58.13% | 58.73% |

### Training Configuration
- **Model**: distilbert-base-cased
- **Epochs**: 3
- **Batch Size**: 16
- **Learning Rate**: 3e-5
- **Max Length**: 128 tokens
- **Dataset**: UCSD Goodreads (6400 train, 1600 test)

## Links

- **Kaggle Notebook**: https://www.kaggle.com/code/reeteshsingh/distilbert-goodreads-classification
- **Hugging Face Model**: https://huggingface.co/reeteshsingh/distilbert-goodreads-genres
- **W&B Dashboard**: https://wandb.ai/g25ait2086-iit-jodhpur/huggingface