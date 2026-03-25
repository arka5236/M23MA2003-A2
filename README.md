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
