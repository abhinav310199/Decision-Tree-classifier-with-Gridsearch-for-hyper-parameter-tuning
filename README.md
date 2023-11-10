# Decision-Tree-classifier-with-Gridsearch-for-hyper-parameter-tuning
Objective:
The project aims to perform multiclass classification using a custom Decision Tree model on a dataset containing information about celestial objects categorized into three classes: 'galaxy', 'star', and 'quasar'.

Context:
In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics.

Content

The data consists of 100,000 observations of space taken by the SDSS (Sloan Digital Sky Survey). Every observation is described by 17 feature columns and 1 class column which identifies it to be either a star, galaxy or quasar.

obj_ID = Object Identifier, the unique value that identifies the object in the image catalog used by the CAS
alpha = Right Ascension angle (at J2000 epoch)
delta = Declination angle (at J2000 epoch)
u = Ultraviolet filter in the photometric system
g = Green filter in the photometric system
r = Red filter in the photometric system
i = Near Infrared filter in the photometric system
z = Infrared filter in the photometric system
run_ID = Run Number used to identify the specific scan
rereun_ID = Rerun Number to specify how the image was processed
cam_col = Camera column to identify the scanline within the run
field_ID = Field number to identify each field
spec_obj_ID = Unique ID used for optical spectroscopic objects (this means that 2 different observations with the same spec_obj_ID must share the output class)
class = object class (galaxy, star or quasar object)
redshift = redshift value based on the increase in wavelength
plate = plate ID, identifies each plate in SDSS
MJD = Modified Julian Date, used to indicate when a given piece of SDSS data was taken
fiber_ID = fiber ID that identifies the fiber that pointed the light at the focal plane in each observation

Data Preparation:

The dataset (df1) is preprocessed by separating features (data) and the target variable (target).
The data is split into training and test sets using the train_test_split function.
Building a Custom Decision Tree Model:

A custom Decision Tree Classifier (dt_custom) is created with specified hyperparameters (e.g., max depth, max leaf nodes, min samples split).
The model is trained on the training data, and accuracy scores are evaluated on both training and test sets.
Evaluating Overfitting:

The project addresses the concern of overfitting by analyzing the accuracy scores on the training and test sets. Overfitting is observed if the training accuracy is significantly higher than the test accuracy.
Hyperparameter Tuning with GridSearchCV:

A grid search is performed to find the optimal hyperparameters for the Decision Tree model using GridSearchCV. This involves exploring different combinations of max depth, min samples split, and max leaf nodes.
Visualizing the Trained Decision Tree:

The project visualizes the trained Decision Tree using the plot_tree function. The tree is displayed with features, classes, and node information.
ROC Curve Analysis:

The ROC curve and AUC are employed for evaluating the performance of the Decision Tree model in a binary classification scenario. This is adapted for a multiclass classification problem by plotting separate ROC curves for each class.
Bias-Variance Tradeoff Analysis:

The Bias-Variance Tradeoff is investigated by varying the complexity of the model (e.g., adjusting the maximum depth of the Decision Tree) and observing the changes in training and testing errors.
Tools and Libraries:

Python with libraries such as scikit-learn, matplotlib, and pandas.
Recommendations:

The project suggests exploring various strategies to mitigate overfitting, such as regularization, feature selection, and model complexity reduction.
Further analysis, including feature importance examination and additional evaluation metrics, can provide a deeper understanding of model performance.
