# DecisionTree
ID3 &amp; C4.5 of DecisionTree
We use ID3 and C4.5 algorithm respectively construct a tree which can classify some data.

# ID3 algorithm:
1 Calculate the number of dataset characteristics of the dataset --> numFeatures
2 Calculate the information entropy of the dataset --> Ent
3 Initialization optimal information gain bestInfoGain=0.0; optimal gain characteristic bestFeature=-1
4 for i in range(numFeatures):
5     Get each column feature dataset --> uniqueVals
6     for value in uniqueVals:
7         Calculate the probability of value in the column feature --> H(D, a)
8         Calculate the entropy --> Ent(D, a) corresponding to each value of the column feature
9     Calculate the information gain --> infoGain(D,a) of the feature of the i-th column
10    if (infoGain > bestInfoGain):
11    bestInfoGain <-- infoGain
12    bestFeature <-- i
13 return bestFeature

# C4.5 algorithm:
1 Calculate the number of dataset characteristics of the dataset --> numFeatures
2 Calculate the information entropy of the dataset --> Ent
3 Initialization optimal information gain bestInfoGain=0.0; optimal gain characteristic bestFeature=-1
4 for i in range(numFeatures):
5     Get each column feature dataset --> uniqueVals
6     for value in uniqueVals:
7         Calculate the probability of value in the column feature --> H(D, a)
8         Calculate the entropy --> Ent(D, a) corresponding to each value of the column feature
9         Calculated feature entropy --> IV(a)
10    Calculate the information gain --> Gain(D,a) of the feature of the i-th column
11    Calculate the information gain rate of the feature of the i-th column --> infoGain= Gain(D,a)/ IV(a)
12    if (infoGain > bestInfoGain):
13    bestInfoGain <-- infoGain
14    bestFeature <-- i
15 return bestFeature
