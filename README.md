# pycon2020-200-billion-gps-points
Analyzing 200 billion GPS Points with Python on the Cheap

Congratulations!
Your proposal, listed below, was accepted to PyCon 2020! If you have any questions, want to make any changes or updates to your title or abstract, have scheduling requirements, or are unable to give your talk, please let me (philgagnon1@gmail.com) know as soon as possible!

# Analyzing 200 billion GPS Points with Python on the Cheap

## Description
There are many blog posts out there that teach you how to create a map or analyze your fitbit data using Python, but what do you do when instead of a couple of thousand GPS points you have 200 billion? Explore how you can scale up your analysis in the cloud without having to learn lots of new skills. As a bonus, learn how to visualize datasets of an unusual size (i.e. very big).

We will explore different strategies using open source tools and discuss the pros and cons of each approach. We will also tell you which we picked and why. We will cover Dask and Ibis with both GPUs and CPUs as well as strategies for data storage.

Note: While we specifically focus on geospatial data, the talk will be relevant for anyone familiar with Pandas and needing to scale to larger datasets.

## Audience
This talk should be attractive to a couple of different audiences. Both relatively novice and more experienced. The talk will be accessible to all since, we will be explaining the concepts as we go. Folks with a basic knowledge of using Pandas will benefit the most. It will show them how they can take existing analysis they do in-memory with Pandas and expand to analysis and visualization of much larger datasets through tools like Dask. There is a geospatial component to the data but it is minor and will be explained. The talk will also be of interest to developers looking for best practices related to analyzing very large datasets stored as flat files in cloud storage (i.e. > 100,000 files on s3). The next audience is folks interested in modern ways of doing geospatial data analysis at scale. Finally, developers interested in benchmarks that explore CPU/GPU/Speed/Cost trade-offs By the end of the talk, I expect the audience to have knowledge of the open source tools available to help them scale their analysis and visualization to large datasets. They will understand the pros and cons of spatially sorting their datasets as well trade-offs between CPU's vs GPU's. They will also have an appreciation of the relative costs of each approach. They will also have access to Jupyter Notebooks with sample code they can run themselves to experiment with the techniques (caveat: on a smaller public dataset)

```Outline
1. Intro (5 min)
    1. Who am I?
    2. Describe the data - 120 days of Nationwide GPS data, Stored on AWS S3, 1 day per folder
    3. Describe the analysis problem - Data is stored nationwide/day, analysis requires dynamic access to small regions 60-90 days
2. Dask for the Win! (5 min)
    1. Show how we can convert our Pandas code into Dask easily
    2. Short video showing Dask in action on the dataset 
3. Work smarter not harder. (5 min)
    1. Why sorting the data spatially might improve our performance
    2. Quick overview of Geohash, Hilbert Curves, RTrees
4. All about those GPU's. (5 min)
    1. What is Ibis, Ibis + GPU Database
    2. Dask + GPU Backend 
5. And the winner is... (5 min)
    1. Show the benchmarks - performance/cost
    2. What did we choose and why
6. Bonus. Interactive visualization of the entire nation using Dask, Datashader and HVPlot. (During Questions)```
        
Additional Notes
This work has not been presented anywhere else.

We will provide a github repo with Jupyter Notebooks with instructions and code samples that demonstrates each of the approaches on a publicly available dataset that the audience can try out at home.

The following two blog posts from 2017 describe work by other people that were early inspiration for some of the work we plan to present.

[geospatial-operations-at-scale-with-dask-and-geopandas] (https://towardsdatascience.com/geospatial-operations-at-scale-with-dask-and-geopandas-4d92d00eb7e8)
[Matt Wrocklin accelerating-geopandas-1](https://matthewrocklin.com/blog/work/2017/09/21/accelerating-geopandas-1)