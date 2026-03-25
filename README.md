How to Run the Code in Google Colab
Follow these steps to successfully execute the notebook:

Step 1: Open Google Colab
Go to Google Colab.

Click on Upload and select the provided Jupyter Notebook file (M23MA2003_prob1.ipynb).

Step 2: Upload the Dataset
Because Colab clears its memory after every session, you need to upload the raw text dataset before running the code.

On the left sidebar of Colab, click the Folder icon (Files).

Click the Upload icon (a page with an up arrow).

Select and upload your raw text file (e.g., Corpus.txt).

Alternative: If the code is set up to mount Google Drive, run the drive-mounting cell and ensure the text file is in the correct Drive directory.

Step 3: Install Required Libraries
The notebook relies on standard Python data science libraries. Most are pre-installed in Colab, but the first cell will download the necessary NLTK components.

torch (PyTorch)

nltk

scikit-learn

matplotlib

numpy

Step 4: Run the Notebook Sequentially
Run the cells in order from top to bottom (or press Runtime > Run all).

Task 1: Will output the total corpus size, vocabulary size (expected ~1,021), and the top-10 most frequent words.

Task 2: Will define the neural networks and run the training loop. (Note: Training 50 epochs on the 18k word corpus should only take a few minutes on Colab's default CPU).

Task 3: Will extract the 50-dimensional vectors and print the nearest neighbors and analogies for target words (research, student, phd, exam).

Task 4: Will automatically generate and display two scatter plot images (PCA clustering) for both the Skip-gram and CBOW models.

Character-Level Indian Name Generation using RNNs
This repository/project contains the implementation of three Recurrent Neural Network (RNN) architectures to generate realistic, character-level Indian names. The models are built using PyTorch and include a Vanilla RNN, a Bidirectional LSTM (BiLSTM), and an Attention-based RNN.

📄 Files Included
M23MA2003_prob2.ipynb: The main Jupyter Notebook containing the data preprocessing, model architectures, training loops, and generation/evaluation functions.

TrainingNames.txt: The text file containing the dataset of 1,431 unique Indian names used for training (Note: Ensure you have this file ready to upload).

🚀 How to Run in Google Colab
Google Colab is the recommended environment for running this notebook, as it provides free access to GPUs which significantly speeds up the PyTorch training process.

Step 1: Open Google Colab
Go to Google Colab.

Sign in with your Google account.

Step 2: Upload the Notebook
Upon opening Colab, a welcome window will appear. Click on the Upload tab.

Click Browse and select the M23MA2003_prob2.ipynb file from your local computer.

The notebook will load and open on your screen.

Step 3: Enable GPU Acceleration (Highly Recommended)
To make the training process much faster:

Click on Runtime in the top menu bar.

Select Change runtime type.

Under the "Hardware accelerator" dropdown, select T4 GPU (or any available GPU).

Click Save.

Step 4: Upload the Dataset
Before running the code, the notebook needs access to the training dataset.

On the left sidebar of the Colab interface, click the Folder icon (Files).

Click the Upload to session storage icon (a piece of paper with an upward arrow).

Select and upload your TrainingNames.txt file.
Note: Colab deletes uploaded files when the session ends, so you will need to re-upload this file if you close and reopen the notebook.

Step 5: Run the Code
You can now run the notebook step-by-step or all at once:

To run cell-by-cell: Click the Play button [ ▶ ] on the left side of each code cell, or press Shift + Enter.

To run the entire notebook: Click on Runtime in the top menu bar and select Run all.

🧠 Model Architectures Explored
Model 1 (Vanilla RNN): A standard character-level RNN.

Model 2 (BiLSTM): A Bidirectional Long Short-Term Memory network with Dropout for regularization.

Model 3 (Attention RNN): An RNN equipped with a custom Attention mechanism to dynamically weigh previous characters during left-to-right generation.

📊 Expected Outputs
As the notebook runs, you will see:

Training Logs: The Epoch number, Training Loss, and Validation Loss printing smoothly.

Early Stopping Messages: If the validation loss stops improving, the model will automatically halt and save the best weights.

Generated Names: A list of new, generated Indian names based on the selected model's output.

Evaluation Metrics: The Novelty Rate (uniqueness) and Diversity Score of the generated names.

⚠️ Troubleshooting
Error: FileNotFoundError: [Errno 2] No such file or directory: 'TrainingNames.txt'

Fix: You forgot to upload the dataset. Follow Step 4 again.

Runtime Disconnected / Variables Lost:

Fix: Colab disconnects if left idle for too long. If this happens, you will need to upload TrainingNames.txt again and select Runtime > Run all to re-initialize your variables.
