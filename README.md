# Machine-Learning-Project-Mushroom-Dataset
Took a dataset containing information about 23 types of gilled mushrooms from the Agaricus and Lepiota Families. Performed a basic classification analysis on the dataset using a decision tree algorithm to determine edibility. I got an accuracy of 1.00 (100%) for the model.

Introduction:
Our dataset contains information about 23 types of gilled mushrooms from the Agaricus and
Lepiota Families that appear across North America. The attributes of the samples include
physical characteristics such as cap color, odor, and stalk shape, as well as information on the
habitat and geographic location of where the mushrooms were found. Each one of the species is
classified as either definitely edible, definitely poisonous, or of unknown edibility (not
recommended to consume). The mushrooms of unknown edibility are grouped together with the
poisonous ones. The dataset states that there isn't an easy way to determine the edibility of a
mushroom. Our dataset contains 8124 instances and 22 attributes. This dataset may be used for
classification tasks in machine learning to predict the edibility of mushrooms based on their
physical characteristics. The attributes are listed as follows:

1. cap-shape: The shape of the mushroom cap, which can be bell = b, conical = c, convex =
x, flat = f, knobbed = k, or sunken = s.

2. cap-surface: The texture of the mushroom cap, which can be fibrous = f, grooves = g,
scaly = y, or smooth = s.

3. cap-color: The color of the mushroom cap, which can be brown = n, buff = b, cinnamon =
c, gray = g, green = r, pink = p, purple = u, red = e, white = w, yellow = y.

4. bruises: Whether or not the mushroom has bruises, which can be yes = t, or no = f.

5. odor: The odor of the mushroom, which can be almond = a, anise = l, creosote = c, fishy
= y, foul = f, musty = m, none = n, pungent = p, or spicy = s

6. gill-attachment: How the gills of the mushroom are attached to the stem, which can be
attached = a, descending = d, free = f, or notched = n.

7. gill-spacing: The spacing between the gills on the underside of the cap, which can be
close = c, crowded = w, or distant = d

8. gill-size: The size of the gills, which can be broad = b, or narrow = n

9. gill-color: The color of the gills, which can be black = k, brown = n, buff = b, chocolate =
h, gray = g, green = r, orange = o, pink = p, purple = u, red = e, white = w, or yellow = y

10. stalk-shape: The shape of the mushroom stalk, which can be enlarging = e, or tapering = t

11. stalk-root: The type of root that the mushroom stalk has, which can be bulbous = b, club
= c, cup = u, equal = e, rhizomorphs = z, rooted = r, or missing = ?

12. stalk-surface-above-ring: The texture of the mushroom stalk above the ring, which can be
fibrous = f, scaly = y, silky = k, or smooth = s

13. stalk-surface-below-ring: The texture of the mushroom stalk below the ring, which can be
fibrous = f, scaly = y, silky = k, or smooth = s

14. stalk-color-above-ring: The color of the mushroom stalk above the ring, which can be
brown = n, buff = b, cinnamon = c, gray = g, orange = o, pink = p, red = e, white = w, or
yellow = y

15. stalk-color-below-ring: The color of the mushroom stalk below the ring, which can be
brown = n, buff = b, cinnamon = c, gray = g, orange = o, pink = p, red = e, white = w, or
yellow = y

16. veil-type: Whether or not the mushroom has a partial or universal veil, which can be
partial = p, or universal = u

17. veil-color: The color of the veil, which can be brown = n, orange = o, white = w, or
yellow = y

18. ring-number: The number of rings on the mushroom stalk, which can be none = n , one =
o, or two = t

19. ring-type: The type of ring on the mushroom stalk, which can be cobwebby = c,
evanescent = e, flaring = f, large = l, none = n, pendant = p, sheathing = s, or zone = z

20. spore-print-color: The color of the spores produced by the mushroom, which can be black
= k, brown = n, buff = b, chocolate = h, green = r, orange = o, purple = u, white = w, or
yellow = y

21. population: The abundance of the mushroom in the area where it is found, which can be
abundant = a, clustered = c, numerous = n, scattered = s, several = v, or solitary = y

22. habitat: The type of environment in which the mushroom is typically found, which can be
grasses = g, leaves = l, meadows = m, paths = p, urban = u, waste = w, or woods = d

Our dataset contains 22 attributes and it was impossible to visualize all of them. We wanted to
determine how the edibility of the mushrooms depends on the various attributes. We used the
attributes cap color, odor, and habitat to visualize the data using bar graphs and countplots trying
to determine how edibility depends on each of them. We can similarly visualize the rest of the
attributes as well.

Data preprocessing:
First, we imported all the libraries we need for this project including pandas, matplotlib, seaborn,
and scikit-learn.
Next, we read our data using pandas dataframe and rename all the columns. Since our values for
each category are alphabetical values we used label encoder to convert them into numerical
values. Then, we clean the data making sure there are no null values or duplicates.


Statistics:
For our statistics, we found the mean, median, mode, standard deviation, and variance of the
columns odor and cap color. 

Machine Learning: Classification Model
To create the machine learning model, we used decision tree classification. Decision tree
classifiers are supervised machine learning models meaning they are trained with pre-labeled
data sets to make predictions which helps them learn and grow more accurate gradually. They
can be used for both classification and regression analysis. We have made a classification model
here. Each node of the tree represents a point of decision-making that splits into leaf nodes. The
leaf nodes can further turn into decision nodes until we have reached a final classification.
Since we have non-numeric data only, we will be using one-hot encoding to convert non-numeric
values to numeric values. One-hot coding takes all the unique values in a column and turns them
into a column of their own. The rows in the columns are assigned the value 1 if it matches the
original value and 0 if it doesn’t.

Next, we split our data into training and validation sets using scikit-learn’s train_test_split
function. By doing this, we reserve some data to verify our model’s effectiveness and accuracy.

We then created a DecisionTreeClassifier model and trained it on the training data. The model is
used to make predictions on the validation set and the accuracy is calculated to assess how good
our model is.

To summarize, we performed a basic classification analysis on our dataset using a decision tree
algorithm. We got an accuracy of 1.00 (100%) for our model, which is rare
