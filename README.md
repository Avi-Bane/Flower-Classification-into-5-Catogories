# Flower-Classification-into-5-Catogories

## About Dataset - Source Kaggle (https://www.kaggle.com/datasets/sauravagarwal/flower-classification)
### Context
Raw jpg images of five types of flowers. Partitioned into test, training and validation directories. Original source are not partitioned. Original source is https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz
Flower types - daisy, dandelion, roses, sunflowers, tulips

###Acknowledgements
Tung, KC (2020), “Flower Images jpg”, Mendeley Data, V1, doi: 10.17632/738sdjm6h9.1

###Inspiration
Multiclass image classification

## Steps Performed in making of the model
1. As the dataset does not contain any CSV file of the path of images, a CSV file and a Dataframe is created with columns Image_Path, Flowers. The dataset contains different folders as train, validate, test. Thus initially, only train and validate datasets are used.

2. Then the train dataset is preprocess exclusively to showcase EDA (Exploratoray Data Analysis). Preprocessing of the train dataframe is performed by removing corrupted images, removing duplicate images, resizing, lastly normalizing between 0 and 1 and save in Images column as the numpy array.

3. Pixel Intensity graph shows the spread of datapoints of clean vs unclean dataset.

4. t-SNE visualization shows the even spreadness of the clean dataset vs unclean dataset.

5. Than the clean train dataframe is converted into tensorflow dataset.

6. The validation dataframe is also preprocessed using previous functions and converted into Tensorflow dataset.

7. Both the datasets are shuffled, Batched, and prefetched.

8. After Checking the Shape the dataset is trained on the MobileNetV2 CNN model.

9. After Fine tuning the model gives an accuracy of 86.2500011920929 %. 
