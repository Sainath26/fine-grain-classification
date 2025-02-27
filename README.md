# Fine-Grained Bird Species Classification  

This project tackles the challenge of fine-grained bird species classification using the CUB-200-2011 dataset, which contains 200 bird species. The solution employs transfer learning with EfficientNetB4, hyperparameter tuning, and phased training to balance accuracy and overfitting.  

**Key Features**  
- Transfer learning with EfficientNetB4 as the base model.  
- Hyperparameter tuning using Keras Tuner.  
- Phased training: frozen base model, classifier head training, and gradual unfreezing.  
- Data augmentation and regularization (dropout, batch normalization).  
- Achieves **76% validation accuracy** and **93% training accuracy**.  

## Approach  
1. **Base Model Selection**: Tested ResNet50 and EfficientNetB4, with EfficientNetB4 showing better performance.  
2. **Hyperparameter Tuning**: Random search for optimal learning rate and dropout.  
3. **Phased Training**:  
   - **Phase 1**: Train classifier head with frozen base model.  
   - **Phase 2**: Fine-tune the last 20 layers of the base model with a reduced learning rate.  
4. **Regularization**: Data augmentation, dropout, and early stopping to mitigate overfitting.  

## Results of the best model
- **Test Accuracy**: 73%  
- **Precision**: 0.75  
- **Recall**: 0.73  
- **F1-Score**: 0.73  
