# Simpsons Character Classifier

This project is a **Simpsons Character Classifier** implemented in Python using a Convolutional Neural Network (CNN). The script predicts which character from *The Simpsons* is present in a given image.
We exepcted to make changes and build a plant disease identifier but had encountered many issues, majorly in dependancies, which we tried a lot but couldn't solve. 

as for the simpson classification, we obtained a 90% accuracy with our own model. 

## Features

- Preprocessing pipeline to resize and normalize input images.
- CNN-based model trained to classify 10 popular *Simpsons* characters.
- Easy-to-use command-line interface for testing the classifier.

## Characters Supported

The model can classify the following characters:

1. Homer Simpson  
2. Ned Flanders  
3. Moe Szyslak  
4. Lisa Simpson  
5. Bart Simpson  
6. Marge Simpson  
7. Krusty the Clown  
8. Principal Skinner  
9. Charles Montgomery Burns  
10. Milhouse Van Houten  

## Requirements

### Libraries
The project uses the following libraries:

- `canaro`  
- `caer`  
- `cv2` (OpenCV)  
- `numpy`  
- `matplotlib`  
- `keras`
- `tensorflow`
- `sklearn`

### Installation
Install the required libraries using `pip`:

```bash
pip install canaro caer opencv-python numpy matplotlib keras
```

### Pre-trained Model
Ensure the pre-trained model file `model_50e_new.keras` is in the same directory as the script. If not, download it from the specified source.

## How to Use

1. **Run the Script**  
   Save the script as `simpsons_classifier.py` and execute it from the command line:

   ```bash
   python simpsons_classifier.py <path_to_image>
   ```

   Replace `<path_to_image>` with the path to the image you want to classify.

2. **Example**  
   ```bash
   python simpsons_classifier.py images/homer.jpg
   ```

3. **Output**  
   The script will display the input image and print the name of the predicted character in the console.

## Code Breakdown

### Functions

1. **`pre(img)`**  
   - Converts the input image to grayscale, resizes it to `80x80`, and reshapes it to the required input format for the CNN model.

2. **`predict_character(test_path, model_path='model_50e_new.keras')`**  
   - Loads the pre-trained model.
   - Preprocesses the input image and makes a prediction.
   - Returns the name of the predicted character.

### Constants
- `IMG_SIZE`: The target size for image preprocessing (80x80).
- `CHARACTERS`: The list of characters supported by the model.

### Command-Line Usage
The `if __name__ == "__main__"` block handles command-line arguments for easy execution.

## Example Output

If you provide an image of Homer Simpson, the script outputs:  

```
The predicted character is: homer_simpson
```

## Notes

- Ensure the test image path is correct. If the image is not found, an error will be raised.
- The `model_50e_new.keras` file must be in the script's working directory or provide its full path.
