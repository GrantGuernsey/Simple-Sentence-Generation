# Simple Sentence Generation with Custom Starting Word

This Python script facilitates sentence generation based on a given text file, allowing users to control the sentence's direction by specifying a custom starting word.

## Usage Instructions

1. **File Selection:**
   - Run the script and use the file dialog to select a text file.
   - Ensure the selected file has a `.txt` extension.

2. **Custom Starting Word:**
   - After selecting the file, modify the `first_word` variable in the script's `main()` function to control the sentence's beginning.

3. **Processing Text:**
   - The selected text file is preprocessed to remove punctuation and convert the text to lowercase.
   - The words in the processed text are split and stored.

4. **Model Creation:**
   - A sequence prediction model is created based on the processed words.
   - The model associates each word with the words that typically follow it in the text.

5. **Sentence Generation:**
   - The script generates a sequence of words by predicting the next word based on the model and the custom starting word.
   - The process continues for 50 iterations, creating a sentence.

6. **Display Result:**
   - The generated sentence is printed to the console.

## Customization

- Modify the `first_word` variable in the `main()` function to change the starting word and influence the sentence generation process.

## Functions

1. **`preprocess_text(file_path)`:**
   - *Parameters:* `file_path` (str) - Path to the text file.
   - *Returns:* List of processed words.
   - *Description:* Reads and preprocesses the text from the selected file.

2. **`create_sequence_prediction_model(words)`:**
   - *Parameters:* `words` (list) - List of processed words.
   - *Returns:* Dictionary representing the sequence prediction model.
   - *Description:* Creates a simple sequence prediction model based on word occurrences.

3. **`generate_prediction(model, input_word)`:**
   - *Parameters:*
     - `model` (dict) - Sequence prediction model.
     - `input_word` (str) - Current word for prediction.
   - *Returns:* Predicted next word.
   - *Description:* Generates a prediction for the next word based on the model.

4. **`main()`:**
   - *Description:* Main function that orchestrates the overall process.
     - Asks the user to select a text file.
     - Checks if the selected file is a text file.
     - Modifies the `first_word` variable to control the starting word.
     - Processes the text and creates a sequence prediction model.
     - Generates and prints a sentence based on the model and custom starting word.

## Running the Script

- Execute the script, and follow the instructions in the console to select a text file.
- Modify the `first_word` variable to influence the sentence generation with a custom starting word.
- Observe the generated sentence based on the provided model and customization.

Feel free to experiment with different starting words to observe how it influences the generated sentences. For further details, refer to the comments in the source code.
