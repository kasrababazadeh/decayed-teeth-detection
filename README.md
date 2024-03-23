# Automatic Decayed Teeth Detection from Bitewing Radiographs using Transfer Learning

This project aims to automatically detect decayed teeth from bitewing radiographs using transfer learning techniques. The process begins with the input of a bitewing radiograph and concludes with the identification of decayed teeth.

## Automatic Decayed Teeth Detection Process

The automatic decayed teeth detection process involves the following steps:

1. **Bitewing Image Input:**

- Users provide a bitewing radiograph as input to the system. Bitewing radiographs are commonly used in dentistry for detecting dental caries and other dental issues.

2. **Tooth Detection:**

- Utilizes Faster R-CNN with ResNet50 backbone for detecting teeth.

- Users can train their own tooth detection model by providing their training images and annotations.

- An annotation tool called LabelImg is recommended for annotating the data, and a converter script is provided to convert annotations to .record file format.

3. **Molar and Premolar Classification:**

- After tooth detection, the identified teeth are cropped and classified into molars and premolars.

- VGG16 architecture is employed for this classification task.

- Users can train their own classification model using the provided script.

4. **Overlapped and Non-Overlapped Teeth Classification:**

- Teeth are further categorized into overlapped, non-overlapped, and not useful teeth.

- VGG16 is utilized again for this classification.

- Users are encouraged to train their own model using the provided code.

5. **Decayed and Non-Decayed Teeth Classification:**
- Finally, teeth are classified as decayed or non-decayed.
- ResNet50 architecture is employed for this classification.

- Users can train their data on the provided script.

### Not Useful Teeth

Not useful teeth refer to the teeth detected during the tooth detection step that are located at the corners of the bitewing radiography and are not completely displayed. These teeth are typically only partially visible in the radiograph and may not provide sufficient information for further analysis.

## Thesis Information

This project is the result of a master's thesis conducted by [Your Name] under the supervision of Dr. Ali Nadian. The thesis explores the application of transfer learning in the field of dentistry for automating the detection of decayed teeth from bitewing radiographs.

## Installation

1. Clone the repository:

git clone https://github.com/yourusername/your-repository.git

2. Set up Google Colab environment and import the necessary libraries.

3. Follow the instructions provided in each step's respective script to train your models and perform evaluations.

## Usage

1. For training your tooth detection model, use `train_tooth_detection.py`.

2. Use `train_molar_premolar_classification.py` for training molar and premolar classification.

3. Train your overlapped and non-overlapped teeth classification model with `train_teeth_classification.py`.

4. Lastly, use `train_decayed_non_decayed_classification.py` to train your decayed and non-decayed teeth classification model.

After training, you can evaluate the performance of the entire pipeline using `evaluation.py`.

## Contributions

Contributions to improve the project are welcome! Feel free to submit pull requests or open issues for any suggestions or bugs.

## License

This project is licensed under the [MIT License](LICENSE).
