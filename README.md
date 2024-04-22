# COMP34812 Instructions

**Task A:** Natural Language Inference (NLI)

*Given a premise and a hypothesis, determine if the hypothesis is true based on the
premise. 26K premise-hypothesis pairs are used as training data and
more than 6K pairs as validation data.*

**Solution B:** Deep learning-based approaches that do not employ transformer architectures

*Our final model used an ensemble approach where predictions from four models LSTM, GRU, BiLSTM and BiGRU are combined using soft voting. Pre-trained GloVe embeddings were used. These models were trained on the dataset.*

**Solution C:** Deep learning-based approaches underpinned by transformer architectures

*Our final model used an ensemble approach where predictions from three transformer models T5, RoBERTa, and FlanT5 are combined using hard voting. These pre-trained models underwent fine-tuning and transfer learning with the dataset to improve their performance, as well as adding a BiLSTM layer to the classification head. Leveraging these pre-trained models as a starting point for training on the dataset will result in faster convergence and improved performance.*

**Group 42 :** Aisha Wahid & Libby Walton

### Demo Code
The demo code for Solution B is in **Group42_DemoCode_NLI_SolutionB.ipynb** and for Solution C is **Group42_DemoCode_NLI_SolutionC.ipynb**.
Upload these notebooks directly into Google Colab and to run the code navigate to Runtime > Run All.

The models are automatically loaded into the environment by downloading from our public Google Drive folders using gdown, meaning they do not have to be manually uploaded to the notebook. However, if for any reason you wish to manually upload them, they can be found in the following links, and adjust paths accordingly.
The links to the models are as follows:
- Solution B Tokeniser: https://drive.google.com/file/d/1fRbUz7lCSS0-kqhO7g-U0qP-OOFKYVM_/view?usp=sharing
- Solution B Models: https://drive.google.com/drive/folders/1oxUyn7EWqkUFEPXvIMiXKJ1nX2Iz-wx2?usp=sharing
- Solution C Models: https://drive.google.com/drive/folders/1GVGIWOzFQ2x-bs3ymfae-dZtRbHThAun?usp=sharing

Currently, the test.csv file is uploaded from our git repository, however, if you wish to test on another file, please upload manually and change paths accordingly.
### Training Code 
See **Group42_Training_NLI_SolutionB.ipynb** and **Group42_Training_NLI_SolutionC.ipynb** for the training code used to train our models. If this is to be run the development files will need to be uploaded and paths changed accordingly. 
