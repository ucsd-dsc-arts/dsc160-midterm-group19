# Picasso and Color Periods

DSC160 Data Science and the Arts - Midterm Project Repository - Spring 2020

Project Team Members: 
- Nikolas Racelis-Russell, nracelis@ucsd.edu
- Iakov Vasilyev, ivasilie@ucsd.edu
- Cameron Shaw, c8shaw@ucsd.edu
- Boyuan Zheng


## Abstract

Our team will analyze Pablo Picasso’s works for computational evidence of the existence of his famous Blue Period. Since Picasso’s Blue Period is an established phenomena, we expect certain tools applied to certain features to return confirming results. We will then take those tools and apply them to other artists’ collections to find out whether it is a common occurrence for artists to have color periods, as well as checking periods for other attributes, such as brightness and saturation. We are expecting many artists will have periods, since we are assuming they are reflective of the artist’s mental state, which can periodically change - or perhaps a period could be in response to a culturally significant event.
We will scrape the artists’ works from WikiArt and extract the simple features ourselves while relying on skimage and other such libraries; after figuring out which features produce the most convincing results. After feature extraction, we can apply techniques from simple hypothesis testing to machine learning classification (i.e. supervised learning). Our goal is to find out which of those techniques can confirm the existence of Picasso’s blue period most effectively, so we can see if it applies to other artists. Since we are working with visual art, we have the opportunity to make the visualizations look unique, because we can use the paintings as graph points, the same way we did for a Rothko canvas. However, since the features and techniques we will use are going to be decided during the process of the analysis, it is hard to tell exactly how we will visualize our results for now. This class is teaching us to quantify and compute seemingly unquantifiable and uncomputable features of art. In this case, with the assumption that color periods come from the artist’s emotional state, we are quantifying the emotional content that state dictates, which is, arguably, the most important aspect of an art piece. Therefore, in addition to pure computational analysis, we can also employ some subjective, personal analysis of each individual artist by trying to figure out the artist’s feelings and motivations over a color period.


## Data

Picasso's works were scraped from WikiArt at https://www.wikiart.org/en/pablo-picasso/. The code from previous exercises had to be slightly modified to also scrape the year of the paintings as to do analysis on the blue period later on. Most paintings are dated so we did not have to struggle much with identifying his blue period.

A fraction of Zdzislaw Beksinski's scanned works from wikiart. [His work] (https://www.wikiart.org/en/zdislav-beksinski/)
All of Beksinski's paintings, photos, and digital work were done between at least 1956-2009, his death. Since a majority of his works are undated, it is impossible to tell when each painting was done, but there are clear distinctions in his style that can be pinpointed. This is what we would like to examine in comparison to Picasso's Blue Period.


## Code

Iakov's Code (code/Iakov V/Project.ipynb)
The notebook scrapes Picasso's painting off of wikiart, then does a permutation test (displaying the p-value), after which there is the popart section. The popart function takes a "camera" input, so use io.imread(filename) for whatever piece of art you want to make into popart. 

[Cameron's Code] (code/Cameron S/Cameron S Beksinski Notebook)
This notebook walks through the scraping, cleaning, analysis and results of the Beksinski analysis portion of the midterm, as well as an attempt to test a classifier using the data gleaned from this sample of Beksinski's works.


## Results

Sunflowers pop-art (results/results_picasso/Goghpop.jpg)
Pop art of Van Gogh's sunflowers using the weird = True argument.
Sunflowers pop-art 2 (results/results_picasso/Goghpop2.jpg)
Pop art of Van Gogh's sunflowers using the weird = False argument.
Guitar pop-art (results/results_picasso/Picpop.jpg)
Pop art of Picasso's guitar using the weird = True argument.

[brightness vs hue] (results/results-zdzislaw-beksinski/brightness_vs_hue.jpg)
Visualization of the mean brightness and the mean hue of each of the chosen Beksinski works.
[saturation vs hue] (results/results-zdzislaw-beksinski/saturation_vs_hue.jpg)
Visualization of the mean saturation and the mean hue of each of the chosen Beksinski works.
[entropy vs energy] (results/results-zdzislaw-beksinski/mean_entr vs mean_ener.jpg)
Visualization fo the mean entropy and the mean energy of each of Beksinski's works.
These visualizations combined show that there are distinct divides in the sample of Beksinski's works that were chosen. 


## Discussion

As a result of the analysis we found evidence supporting the Picasso "blue period" theory. Furthermore, we found a couple of periods for Beksinski as well, although there was a bit of confusion with the dates. Finally, we made a pop-art generator that takes any picture as input and makes a Warhol Monroe-type painting.

The initial idea was to test many different artists for periods of color, saturation, etc. We started by doing a permutation test on all of the Picasso's paintings that we could scrape from WikiArt. As a test statistic we used the mean of blue - (mean of red + mean of green). Initially we wanted to only check for the absolute levels of blue color, but from the start it turned out that the mean of blue color is the same in his blue period as it is in all the other paintings. Therefore, we had to come up with some type of a comparative statistic that would a) incorporate all of the data and b) would show the blueness of Picasso's paintings, so the difference of color means came about. For the blue period dates I took the ones mentioned in this https://en.wikipedia.org/wiki/Picasso%27s_Blue_Period wikipedia article, 1901-1904. The null hypothesis was that the paintings from that era could have come from the overall distribution, the alternate hypothesis -- those paintings are way bluer than the rest of Picasso's work. The p-value of the test turned out to be 0, meaning there is a huge disparity in the "blueness" of the blue period versus the other works, rejecting the null hypothesis and giving evidence towards the alternative.

A similar analysis was done on Beksinski's works. Observation shows that there are several "periods", the main standouts being the black and white type, the predominantly orange type, the blue type, and periods that are greyer or somewhere in between. In Cameron's code, he attempted to train a classifier to identify orange and non-orange paintings, but the score was low. If a follow-up were to be planned, it'd probably be better to use a much larger sample. However, for this project we decided not to use all of them, as that would've been much too large.

Zdzislaw Beksinski's works are famous for their surreal, fantastical, almost post-apocalyptic style, and his influence can be seen across western media, especially in the horror genre, in which his works seem to best be described. However, Beksinski, being the eccentric he was, rarely dated or signed his paintings. For us, as data scientists, this presents a unique issue in that everything must be done relative to the rest of his paintings. With Picasso we were able to accurately date periods that share style and color. So unlike Picasso, this is a situation wherein we cannot with certainty say that there is a Beksinski "Orange Period." One thing that can be said is that his paintings are uniquely gloomy in tone, their saturation and brightness clearly similar to one another, yet their colors can vary from a gloomy grey to a bright blue. Moreover, the paintings are also distinctly dynamic in their presentation. There was very little low entropic, low energy works. There were always vibrant colors to accompany the macabre imagery. 
If future statistics were to be done on these paintings, perhaps comparisons between these paintings and other macabre horror titans can be made, like the *Alien* franchise for example, whose iconic design for the *Alien* super predator matches the macabre themes of Beksinski's paintings to a T.

After those analyses, Iakov came up with an idea that does not have much to do with the analyses at all. The idea was to computationally create pop-art out of any painting. In order to do that we applied K-Means clustering to the RGB values of the paintings to find similar colors, and then either added random numbers to those RGB values or substitued them with the random numbers (hence the boolean "weird" argument in the popart function). In any case, the results turned out pretty great-looking, putting 4 of them together made it look like an Andy Warhol painting (his artwork was the main source of inspiration for this part). There are a couple of cool things that could be done with the popart generator, sadly the idea came to us too late to implement most of them. One of the things, for example, is to analyze other artists, figure out their color palettes, and make, say, Van Gogh-style pop art, Malevich-style pop art and so on. It does not even have to be hardcoded; it can be done algorithmically with any artist available for scraping. A less realistic but also interesting future direction is to have some type of feedback system that ranks the visual appeal of the popart generated by the function, so that we can figure out which colors work better in combination with each other and use those instead of generating the colors completely randomly. Overall, the alrogithm is not very flexible and has a couple of hardcoded features that limit its "creativity" (such as an arbitrary K = 3 for the clustering).


## Team Roles

Cameron Shaw - wrote code for the Beksinski scraping and analysis, as well as worked on the write-up.
Iakov Vasilyev - wrote code for Picasso scraping, analysis, and the pop-art part. Also worked on the write-up.


## Technical Notes and Dependencies

The arguments for the popart function are:
camera (ndarray) - the input picture
weird (boolean) - whether the popart generation is additional or substitutional
blur (boolean) - whether to use opencv bilateral smoothing
num (integer) - number of pictures to generate, set to 4 in order for the visualization cell below to work (couldnt come up with a way to generalize it).


## Reference

References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts
