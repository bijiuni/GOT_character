# A Web Crawler Studying the Character Occurrences in the TV show Game of Thrones

a Python program is developed to extract, save and process information from a website called ‘Game of Thrones Wiki’. The hyper-textual network contains a great quantity of data like episode plots, character introductions, world cultures centering the television show ‘Game of Thrones’, which is known for its enormous and complex character network. This study makes use of a series of links that contain episode plot introduction. The occurrences of a character are important indicators of the importance of the character during certain periods of the show. It is thus interesting to extract this information from the website and compare the change in character occurrences as visually as possible.


### Prerequisites

The program was run using ipyton 1.2 version

The igraph package has been renewed so please first update in terminal

please update plotly to the latest version as well

```
$ pip install plotly --igraph
$ pip install plotly --upgrade
```

## Running the tests

You can directly run the _program.ipython_


## Log and Output files

Two new files will be generated after running the program: the log file ‘GOTspider.log’ and the output file ‘GOToutput.json’. The log file takes note of two events showing the ongoing process: visiting episode website and counted character occurrences. The format of messages was set to be %(asctime)s %(levelname)s %(message)s and the minimum level was set to be ‘INFO’ to allow all the information to pass to the log file. The output file shows the raw data that is used to build up the ribbon plot. This allows the user to study the special occasions and tendency more meticulously. The keys of the dictionary in the output file are the episode numbers and the occurrences are arranged in the same order as in the ribbon plot. It should be noticed that the log file is written as the program progresses while the output file is only generated at the last step of the function GOT_spider.

## Information Selection and Data pattern

Even in a single episode page in the game of thrones wiki website, there are a large number of links that lead to character pages, other episode pages, location pages and etc. To extract the link to the next episode of the episode the program is currently visiting, a certain pattern of the ‘next episode links’ needs to be found. It was discovered that the link to the next episode is always in a table (and the only table in the page) and it is always the last link in the table. Therefore, codes were written to first locate the table in the page, then saves all links into a list ‘epillist’ and finally extract the last link in the list.
All the words in the plot introduction can be located by finding the ‘p’ tap in the soup object. Thus simply counting the character name in the parts that are tagged as ‘p’ we can obtain the occurrences in a single episode.


## Character list:
Trace 0: Robert Baratheon  
Trace 1: Jon Snow  
Trace 2: Arya Stark  
Trace 3: Cersei Lannister  
Trace 4: Jaime Lannister  
Trace 5: Tyrion Lannister  
Trace 6: Daenerys Targaryen  
Trace 7: Petyr Baelish  
Trace 8: Jaqen H'ghar  
Trace 9: Hodor  

## Results

![](https://github.com/bijiuni/GOT_character/blob/master/result1.jpg)
![](https://github.com/bijiuni/GOT_character/blob/master/result2.jpg)
![](https://github.com/bijiuni/GOT_character/blob/master/result3.jpg)

## Package

* [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) - pulling data out of HTML and XML files
* [Numpy](http://www.numpy.org/) - scientific computing with Python
* [Plotly](https://plot.ly/) - Web-based data visualization and analytical apps

## Authors

* **Zach Lyu**  - [Zach Lyu](https://github.com/bijiuni?tab=repositories)
