# TODO list for evaluation

# Recode our categorical data

To apply this project python code to our data the data has to be recoded. The GAN and NN in general requires *numerical* data. The continues varaibles may need to be scaled but categorical variable values has to be represented as numbers.

For each categorical variable the dictionary has to be build reflecting all possible values mapped to list of numbers.
The [adult dataset description file](https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.names) provides the list of values for all categorical variables and values they have:

```
workclass: Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked.

education: Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool.
```

The code has transform these lists into *Encoding Tables* of the following form:

```json
%{ 'workclass': 
   %{ 'Private': 1,
      'Self-emp-not-inc': 2, 
      'Self-emp-inc': 3,
      'Federal-gov': 4 
    }
}
```


