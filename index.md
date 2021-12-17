
# The evolution of the presence of women’s voices in the media

24% of the news sources -people quoted, heard, seen- are women, according to a 2015 study by the Global Media Monitoring Project (1).
The Me Too movement started to spread in 2017 after the sexual abuse allegations against Harvey Weinstein. This movement led to a raise of women’s voices everywhere.

![How-the-MeToo-Movement-Highlights-the-Need-for-Security-Sector-Reform-in-the-Global-North](https://user-images.githubusercontent.com/91726001/146575120-6d7682b7-c83d-4012-82c6-852e23a704ee.jpeg)
Source of the picture: (2) 

The goal of this project is to track the evolution of the presence of women’s voices in the media following the Me Too movement, to see if a major feminist movement like this one has led to an increase in the number of women quoted. We can then see if women are underrepresented in the medias and if they are only quoted on certain subjects. We can also include the ethnicity and the age of the women that the medias highlight to find which social backgrounds are best represented.

Are women more quoted in the media since the Me Too movement in 2017 ? Are they only quoted on certain subjects (eg. Feminism) ? Women of which social backgrounds, ethnicity and age are best represented in the media ? Does the MeToo movement increased women's voice in the media for topics that are not directly related the MeToo movement and feminism ?

To conduct this project and find answers to these questions, data from the quotebank dataset was used. The quotebank dataset is a corpus containing 178 million speaker-attributed quotations sourced from 196 million English news articles between August 2008 and April 2020 (3).

## Data approach 

To perform the present work we considered "male" as biological and transgender males, and "female" as biological and transgender females, and the other possibles gender  were considered as "other" gender. 

## A first glance to the data

Considering the data approach for this study, one can first look at how women are considered in the media as speakers relative to men and other genders. According to the latter, One can take all the years studied (2015 to 2020) and analyze the overall proportion. 

![image](https://user-images.githubusercontent.com/91272237/146225019-7ef98f47-adab-4d9e-820b-6942ddc9789d.png)

Based on the above pie chart, it is clear that men dominated with 85.6% of the gender's speakers compared to women that only represent 14.3% of the speakers and the “other” gender with almost negligible proportion (<1%).

![image](https://user-images.githubusercontent.com/91272237/146229279-5de6300a-e1be-4b49-8298-cafda2cbcc73.png)

If we analyze women’s representation for each year, we can see that the female speaker proportion from 2015 to 2020 changed from 12.6% to 16.22%, increasing 3.61%.  

![eachyears](https://user-images.githubusercontent.com/91272237/146222509-d69f2460-32cd-4b87-b5b2-731be6f35123.png)

The men speaker proportion from 2015 to 2020 decreased from 87.25% to 83.71%, a 3.54% change. Meanwhile, other genders' speaker proportion only increases by 0.003%, meaning that women absorb all the differences observed in the representation of each gender category. 

Despite the latter, it is interesting to evaluate if the change observed in women's proportion as a speaker is statistically significant and, hence, real game-changing. By comparing the women proportion before 2017 to after 2017, we obtained that the change in women proportion is statistically significant and if we compare only 2017 with 2020. 

Since we can observe an exciting change in the representation of women in the media, we can now perform further analysis to have a closer insight on this ongoing phenomenon which could be associated with the  “Me Too” movement in 2017 or simple related to the cultural evolution since the first and the current feminism movement.


## Time Series Analysis

To analyse the evolution of the presence of women's voice in the media, the percentage of quotes by female speakers in the quotebank dataset were calculated per month and ploted as a time series. 

![timeseries](https://user-images.githubusercontent.com/91726001/146341654-82347c16-40e4-488f-9cfe-77036315b76d.png)

What is immediately noticeable when looking at the graph is that it shows particularly high fluctuations in year of 2016. We asked ourselves why that might be, and it turns out that the Quotebank database has fewer quotes for the year 2016. This smaller amount of data leads to these greater fluctuations. 

Time series plots were also created for each year separately and can be seen below. 

![tsy](https://user-images.githubusercontent.com/91726001/146558776-2bd8be5f-31a2-49de-944e-c3121076b7c1.png)

As for the year 2020, only data from January until April is available, it is not really a time series but nevertheless we have also illustrated it. 

### Trend detection

To detect the trend in the time series of the data, 4 different approaches were used: data was shuffled and plotted as comparison to the original plot, the rolling averange was conducted, the Dickey Fuller test was applied and linear regression was performed. 

- Shuffling of percentage values

In this part, the percentage values from the original data were shuffled and plots were created. The approach to compare the plot of the original dat with the plots from randomly shuffled data can be used to get a first feeling for the trend of the data.

![shuffle1](https://user-images.githubusercontent.com/91726001/146341320-fb574c4a-2c92-4f88-ba2b-731b3421774b.png)
![shuffle2](https://user-images.githubusercontent.com/91726001/146341284-61eba204-5580-4f16-a3ff-8396eea9fc7f.png)
![shuffle3](https://user-images.githubusercontent.com/91726001/146341128-0f9fa9bc-10d9-42cf-aeec-7cf8602de5f8.png)
![timeseries](https://user-images.githubusercontent.com/91726001/146341403-908bd45b-111c-41cd-8223-669558992493.png)
        
The plots created by shuffling all look quite similar, indicating no trend in the datapoints. In contrast to this, the plot of the original data seems to indicate an increase in the percentage of female speakers.  

- Performance of rolling mean 

In statistics, rolling average (also called moving average or running average) is calculated to create a series of averages of different subsets of the full data set. When used with time series data, it smooths out short-term fluctuations and highlights long-term trends or cycles. 

![rolling](https://user-images.githubusercontent.com/91726001/146338375-abb3a593-a36d-4559-a1eb-d17a36724cfb.png)

In the case of this project, rolling mean (7) was performed and the plot shows the orgininal percentage of female speaker, the rolling mean of female speaker percentage and the standard deviation of the rolling mean. This plot also nicely shows the higher standard deviations of the rolling where the data is smaller. 

- Check for stationarity in the data by applying the Dickey Fuller test

One of the key elements in time series analysis is stationarity. Stationarity defines that the statistical properties of the time series are not changing over time, therefore stationary time series will not have any trends or seasonal patterns. Here we will use the Dickey Fuller test to check for stationarity in our data. The Dickey Fuller test will generate critical values and a p-value, which will allow us to accept or reject the null hypothesis. The null hypothesis is non-stationarity. If we reject the null hypothesis, we accept the alternative, which states that there is stationarity in the data. As the p-value of the Dickey Fuller test for our data was 0.87, the null hypothesis is not being rejected and our time series is non-stationary. 

- Linear regression

To calculate the trend in the data, linear regression was conducted. The linear regression line shows a clear increase of the percentage of female speakers in the data.  

![reg](https://user-images.githubusercontent.com/91726001/146344228-d7ee567b-7405-49f4-9140-0f1e5bab5286.png)

The linear regression results show an increase in the percentage of female speakers by 0.68 % per year.

### Check for seasonality

For the time series analysis of our data, a check for seasonality was also performed to see if the percentage of female speaker has a seasonal trends. To do so, the percentage data for all the years 2015-2020 were plotted monthly into one plot. 

![seasonality](https://user-images.githubusercontent.com/91726001/146344280-5cf7eb3a-bc53-4bf6-bfae-4751fb554df6.png)

The plots shows no trend. The data points are randomly distributed and therefore no seasonality is present in the data. 

## Topic detection for women's speeches in 2020

We now want to look into the topics on which women are cited from 2015 to 2020, do those topics change through the years? And are those topics different from the one found for men speakers?

Here are first the topics found after a topic detection on the quotes of 2020 (men, women and others). 
![all_topics_2020](https://user-images.githubusercontent.com/91544456/146554902-68319286-9f47-40ca-9fbd-67a852ea7d40.png)

We notice here quite easily that the four topics are related to stigmas more related to men (let us keep in mind that more than 83% of speakers cited in 2020 are still men): two topics feature the word "guy", all the topics are related to the industry or the market. We can also notice the word "strong" that is quite masculinely connoted. 

Then, the topic detection was computed for women speakers only, first for 2015, and then 2020, to try to see some potential difference that could be (or not) caused by the MeToo movement.
![topics_2015](https://user-images.githubusercontent.com/91544456/146554089-9b18da28-04fa-48de-a3bd-bd524a0d9e4d.png)

![topics_2020](https://user-images.githubusercontent.com/91544456/146554137-8e1b507b-26f1-4882-bf78-fcb46a4713b3.png)


## Sources

(1) https://www.weforum.org/agenda/2020/03/women-representation-in-media/

(2) https://issat.dcaf.ch/Share/Blogs/ISSAT-Blog/How-the-MeToo-Movement-Highlights-the-Need-for-Security-Sector-Reform-in-the-Global-North

(3) https://zenodo.org/record/4277311#.YbyxXy_37PD
