
# The evolution of the presence of women’s voices in the media

24% of the news sources -people quoted, heard, seen- are women, according to a 2015 study by the Global Media Monitoring Project (1).
The Me Too movement started to spread in 2017 after the sexual abuse allegations against Harvey Weinstein. This movement led to a raise of women’s voices everywhere.
The goal of this project is to track the evolution of the presence of women’s voices in the media following the Me Too movement, to see if a major feminist movement like this one has led to an increase in the number of women quoted. We can then see if women are underrepresented in the medias and if they are only quoted on certain subjects. We can also include the ethnicity and the age of the women that the medias highlight to find which social backgrounds are best represented.

Are women more quoted in the media since the Me Too movement in 2017 ? Are they only quoted on certain subjects (eg. Feminism) ? Women of which social backgrounds, ethnicity and age are best represented in the media ? Does the MeToo movement increased women's voice in the media for topics that are not directly related the MeToo movement and feminism ?

## Data approach 

To perform the present work we considered "male" as biological and transgender males, and "female" as biological and transgender females, and the other possibles gender  were considere as "other" gender. 

## A first glance to the data

Considering the data apporach for this study, one can take as first look to how women is considered in the media as speakers relative to men and other geneders, to do that one can take all the years studied (2015 to 2020) and analysis the overall proportion. 

![image](https://user-images.githubusercontent.com/91272237/146225019-7ef98f47-adab-4d9e-820b-6942ddc9789d.png)

Base on the above pie chart it is clear that men dominated with 85.6% of the gender's speakers compare to womans that only represent 14.3% of the speakers, and other gender with almost negible proportion (<1%).

![image](https://user-images.githubusercontent.com/91272237/146229279-5de6300a-e1be-4b49-8298-cafda2cbcc73.png)

If instead we analyze women’s representation for each year, we can see that the female speaker proportion from 2015 to 2020 change from 12.6% to 16.22%, which is an increase of 3.61%. 

![eachyears](https://user-images.githubusercontent.com/91272237/146222509-d69f2460-32cd-4b87-b5b2-731be6f35123.png)

Regarding the men speaker proportion between 2015 to 2020, changing from 87.25% to	 83.71% which represent a derease of 3.54%, meanwhile other gender's speaker proportion only change increase by 0.003% meaning that womens abosrb all the change observed in the repsentation of each gender category. 

Despite the latter, it is intersting to evaluate if the change observed in women proportion as speaker is statistically significant and hence a real game changing. According to this, by comparing the women proportion before 2017 to after 2017 we obtaing that the change in women proportion is statitically significant, as well as if we compare only 2017 with 2020. 

Since we can observe an intersting change in the representation of women in the media we can now perform different analysis to have a closer insight on this ongoing phenomenon which could be associated with the two moment in 2017 or simple related to the cultural evolution since the first and the current feminism movement. 

## Time Series Analysis

To analyse the evolution of the presence of women's voice in the media, the percentage of quotes by female speakers in the quotebank dataset were calculated per month and ploted in a time series plot. 

![timeseries](https://user-images.githubusercontent.com/91726001/146085588-108b6842-7aea-442d-9a14-252cd152d258.png)

![PerYear](https://user-images.githubusercontent.com/91272237/146222922-514ffc7c-0f09-4e05-ab61-1c36bbda28e1.png)

### Trend detection

To detect the trend in the time series of the data, 4 different approaches were used: data was shuffled and plotted to compare to the original plot, the rolling averange was performed, the Dickey Fuller test was applied and linear regression was conducted. 

- Shuffling of percentage values

In this part, the percentage values from the original data were shuffled and plots were created. By comparing the plot of the original data to the plots from randomly shuffled data can be used to get some first ideas.  


  ![shuffle1](https://user-images.githubusercontent.com/91726001/146204239-75914740-c51c-4173-bb4a-b21fb447c18f.png)  
  ![shuffle2](https://user-images.githubusercontent.com/91726001/146204273-2c2bd68f-49c6-4a4f-b386-155fc4e941da.png)
  ![shuffle3](https://user-images.githubusercontent.com/91726001/146204294-33f876ef-0ab8-4e76-8abd-53a3577f99f2.png)
  ![timeseries](https://user-images.githubusercontent.com/91726001/146204753-37778a1b-3574-4df0-b55e-c9df15b3f4fe.png)

          
We can see that the plots created by shuffling all look quite the same, indicating no trend in the datapoints, whereas the plot of the original data seems to indicate an increase in the percentage of female speakers.  

- Performance of rolling mean 

In statistics, rolling average (also called moving average or running average) is calculated to create a series of averages of different subsets of the full data set. When used with time series data, it smooths out short-term fluctuations and highlights long-term trends or cycles. 

![rolling](https://user-images.githubusercontent.com/91726001/146338375-abb3a593-a36d-4559-a1eb-d17a36724cfb.png)

In the case of this project, rolling mean (7) was performed and the plot shows the orgininal percentage of female speaker, the rolling mean of female speaker percentage and the standard deviation of the rolling mean. In this plot we can also see that the standard deviation is increased in the year 2016 and beginning of 2017, this would also explain the major fluctuations during this time in the time series plot. 

- Check for stationarity in the data by applying the Dickey Fuller test

Stationarity is a key part of time series analysis. Stationarity means that the manner in which time series data changes is constant. A stationary time series will not have any trends or seasonal patterns. Here we will use the Dickey Fuller test to check for stationarity in our data. This test will generate critical values and a p-value, which will allow us to accept or reject the null hypothesis that there is no stationarity. If we reject the null hypothesis, we accept the alternative, which states that there is stationarity. As the p-value of the Dickey Fuller test for our data was 0.87, the null hypothesis is not being rejected and says that our time series is non-stationary. 

- Linear regression

To calculate the trend in the data, linear regression was conducted. The plot shows a clear increase of the percentage of female speakers in the data.  

![reg](https://user-images.githubusercontent.com/91726001/146176743-ffd09169-0550-4c3d-830a-bb55086eb9bd.png)

The linear regression results show an increase in the percentage of female speakers by 0.68 % per year.

### Check for seasonality

For the time series analysis of our data, a check for seasonality was also performed to see if the percentage of female speaker has seasonal trends. To do so, the percentage data for all the years 2015-2020 were plotted monthly. 

![seasonality](https://user-images.githubusercontent.com/91726001/146163788-6e196a18-4e17-4b1c-8035-35d35199ec9a.png)

The plots shows no trend. The data points are randomly distributed and therefore no seasonality is present in the data. 

### Topic detection for women's speeches in 2020




## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/LucieCastella2/ADA-Data-Story/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LucieCastella2/ADA-Data-Story/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
