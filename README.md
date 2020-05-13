## Idea Behind K-NN
The k Nearest Neighbors (k-NN) is one of the oldest supervised machine learning algorithms. It was created by Cover and Hart in 1967. You can read more on my [medium](https://medium.com/analytics-vidhya/k-nearest-neighbors-from-a-theoretical-perspective-5d0da1ded4e0).  

To understand how k-NN works, let’s start by analysing the following figure.  

![data](https://user-images.githubusercontent.com/17646546/81757443-4fea1400-9495-11ea-9523-ef636e6de91f.png)

We notice a data set with the points scattered on the graph and we have two classes: purple and orange. We observe yet a new point, a small triangle. The question that arise is: this new point is purple or orange?  

You probably assumed that the class of the new point is the purple one. Now think about how you did this! How did you figure out that it’s purple? Did you use any derivative rules? Did you use probability? Did you use linear algebra? No!  

What you probably did was to look at the proximity of the points. The little triangle is closer to the purple points than to the orange points. Then, you decided to classify it as purple based on the proximity of the purple points. This is the same idea behind the k-NN algorithm!  

## Algorithm k-NN

Given the data set **D = {(x1, y1),. . . , (xN, yN)}**, the label for any vector x can be estimated with k-NN by following these steps:  
```
1. Compute distance d := d(x, xi) for i = 1, …, N; to every points x;
2. Find the indexes of the k smallest elements and their labels from d;
2. Return h(x) = mode(y1, …, yk).
```

### Decision boundary between [-1, 1]² for k = 1

![1](https://user-images.githubusercontent.com/17646546/81757769-53ca6600-9496-11ea-80a3-f1a73df3c405.png)

### Decision boundary between [-1, 1]² for k = 3

![3](https://user-images.githubusercontent.com/17646546/81757819-7d838d00-9496-11ea-90ed-617be6794ec8.png)

### Decision boundary between [-1, 1]² for k = 9

![9](https://user-images.githubusercontent.com/17646546/81757828-88d6b880-9496-11ea-8d10-b450f5c23512.png)

### Decision boundary between [-1, 1]² for k = 27

![27](https://user-images.githubusercontent.com/17646546/81757846-92602080-9496-11ea-8d3e-363d47c91d64.png)
