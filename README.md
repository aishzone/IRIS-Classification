These are some of the important terms which will help you throughout your wonderful journey in machine learning using python.
## Basic Terminologies in Classification Algorithms
* __Dataset__: Table with the data from which the machine learns.When used to induce a model, the dataset is called training data.
* __Classifier__: An algorithm that maps the input data to a specific category.
* __Classification model__: A classification model tries to draw some conclusion from the input values given for training. It will predict the class labels/categories for the new data.
* __Instance__: A row in the dataset. Other names for 'instance' are: (data) point, example, observation.
* __Feature__: A feature is an individual measurable property of a phenomenon being observed.
* __Binary Classification__: Classification task with two possible outcomes. Eg: Gender classification (Male / Female) , (Yes/No) or (True-1/False-0) question.
* __Multi-class classification__: Classification with more than two classes. In multi-class classification, each sample is assigned to one and only one target label. Eg: An animal can be a cat or dog but not both at the same time.
* __Multi-label classification__: Classification task where each sample is mapped to a set of target labels (more than one class). Eg: A news article can be about sports, a person, and location at the same time.

This is all you need to build your first classification model, Surprising right?

## IRIS Classification model
__USE CASE__  → Botanist wants to determine the species of an iris flower based on the characteristics of that flower.Attributes including petal length and width ,sepal length and width etc.. are the "features" that determine the classification of the given iris flower.
![Image of setosa,versicolor,verginica](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Machine+Learning+R/iris-machinelearning.png)
## Coding
Let's start off by displaying the above images on the screen

' ' '
from IPython.display import Image
url = 'http://upload.wikimedia.org/wikipedia/commons/5/56/Kosaciec_szczecinkowaty_Iris_setosa.jpg'
Image(url,width=300, height=300)
from IPython.display import Image
url = 'http://upload.wikimedia.org/wikipedia/commons/4/41/Iris_versicolor_3.jpg'
Image(url,width=300, height=300)
from IPython.display import Image
url = 'http://upload.wikimedia.org/wikipedia/commons/9/9f/Iris_virginica.jpg'
Image(url,width=300, height=300)
' ' '

Now we start the actual coding by importing the required datasets for us to train and work with.The Iris dataset was used in R.A. Fisher's classic 1936 paper, The Use of Multiple Measurements in Taxonomic Problems, and can also be found on the UCI Machine Learning Repository.It includes 3 iris species with 50 samples each as well as some properties about each flower.

' ' '
from sklearn.datasets import load_iris
iris=load_iris()
print(iris)
' ' '

We first import the iris dataset which has a total of 150 samples.Let me explain you the output that you have got … __'data': array__ → Contains all the 150 sample's data __'target': array__ →Contains 0's,1's and 2's indicating 0 for setosa,1 for versicolor and 2 for virginica , __'target_names': array__ →Contains the names of the 3 species(['setosa', 'versicolor', 'virginica'] , __'DESCR'__ →It is the entire history or description which includes the attributes,instances etc.. also it tells us if there is a loop hole i.e. a missing attribute . __'feature_names'__ →Contains the names of the 4 attributes with their units and finally we have the __'filename'__.

