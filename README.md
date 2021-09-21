# Apply unsupervised clustering algorithm on dataset

Use K-Mean clustering cluster the customer from dataset "Mall_Customer" into several group by detecting the distinct categories of groups to to understand which group of customer can be easily converge, so it gives the marketing team to plan the strategy accordingly.

# Required inputs
dataset as csv file

# Outputs
## Plots
First plot is the correlation between two variable, and this is where the number of cluster get determinated.
Second plot is the K-mean cluster plot

## Files 
A files with new column named "Cluster" is saved, which group custumers into 5 cluster

# Usage
## Required Libraries
```bash
pandas
numpy
seaborn
matplotlib.pyplot
sklearn.cluster
```
## Example commands
```bash
df = pd.read_csv('.csv')
sns.pairplot(df[['a', 'b', 'c']])
kmeans=cluster.KMeans(n_clusters=N, init="k-means++")
kmeans=kmeans.fit(df[['a', 'b']])
df['Cluster']=kmeans.labels_
sns.scatterplot(x="a", y="b", hue='Cluster', data=df)
df.to_csv('.csv', index= False)
```

# runtime and memory requirements
The total runtime is about 5.17s.  
The memory requirement is about 960 MB. 
