# Alphabet Soup Investors Analysis (ML)

**Data Analytics Bootcamp – University of California, Irvine**  
**Module 21**  
**Topic:** Neural Networks and Machine Learning  
**By:** Jay Boon

---

## **Project Objective**

This project focuses on helping the non-profit foundation **Alphabet Soup** predict the likelihood of funding success for applicants. A deep learning model was developed to analyze applicant data and produce a binary outcome—indicating whether funding is likely to be awarded.

- **Target variable:** `IS_SUCCESSFUL`  
  - `1` = Funding awarded  
  - `0` = Funding not awarded

---

## **Data Preparation & Preprocessing**

Data preparation and preprocessing were essential to ensure the model could learn meaningful patterns. Key steps included:

- **Standardized Feature Scaling**
  - Numeric values were scaled to ensure consistency across features.

- **Removed Non-Contributory Columns**
  - Dropped `EIN` and `NAME` as they did not aid in prediction.
  - `NAME` was temporarily reintroduced for binning rare entries.

- **Identified High-Cardinality Features**
  - Rare values were grouped into an `"Other"` category.

- **Encoded Categorical Variables**
  - Applied one-hot encoding to convert text features into numeric format.

- **Split Data for Training and Evaluation**
  - Divided into training and testing sets to validate performance.

---

## **Model Development**

A deep neural network was implemented using TensorFlow and Keras:

- Input layer matched the number of processed features  
- Two hidden layers with ReLU activation  
- Final output layer with sigmoid activation for binary classification  
- Binary cross-entropy used as the loss function  
- Accuracy used as the evaluation metric

---

## **Results: Baseline Model**

- Architecture: 3 layers  
- Trainable parameters: 477  
- Achieved accuracy: **~73%**  
- Slightly below the project target of 75%

---

## **Optimization and Improvement**

Several enhancements were made:

- Reintroduced the `NAME` column for improved binning  
- Increased the number of hidden neurons  
- Expanded architecture to **3,298 parameters**

**Final accuracy: Over 79%**, surpassing the original benchmark.

---

## **Key Takeaways**

- Proper data standardization and encoding significantly affect outcomes  
- Binning rare categories helps generalization  
- More complex models (layers and neurons) can lead to better performance

---

## **Tools Used**

- Python  
- Pandas  
- TensorFlow / Keras  
- Scikit-learn

---

For additional questions or professional inquiries, [connect on LinkedIn](https://www.linkedin.com/in/justboon/).
