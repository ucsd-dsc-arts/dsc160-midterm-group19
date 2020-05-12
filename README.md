# Picasso and Color Periods

DSC160 Data Science and the Arts - Midterm Project Repository - Spring 2020

Project Team Members: 
- Nikolas Racelis-Russell, nracelis@ucsd.edu
- Iakov Vasilyev, ivasilie@ucsd.edu
- Cameron Shaw, c8shaw@ucsd.edu
- Boyuan Zheng

## Abstract

(10 points) 

For the project proposal, please write a short abstract addressing the questions below. You should replace the entire contents of this section with one to two paragraphs addressing the following:

Our team will analyze Pablo Picasso’s works for computational evidence of the existence of his famous Blue Period. Since Picasso’s Blue Period is an established phenomena, we expect certain tools applied to certain features to return confirming results. We will then take those tools and apply them to other artists’ collections to find out whether it is a common occurrence for artists to have color periods, as well as checking periods for other attributes, such as brightness and saturation. We are expecting many artists will have periods, since we are assuming they are reflective of the artist’s mental state, which can periodically change - or perhaps a period could be in response to a culturally significant event.
We will scrape the artists’ works from WikiArt and extract the simple features ourselves while relying on skimage and other such libraries; after figuring out which features produce the most convincing results. After feature extraction, we can apply techniques from simple hypothesis testing to machine learning classification (i.e. supervised learning). Our goal is to find out which of those techniques can confirm the existence of Picasso’s blue period most effectively, so we can see if it applies to other artists. Since we are working with visual art, we have the opportunity to make the visualizations look unique, because we can use the paintings as graph points, the same way we did for a Rothko canvas. However, since the features and techniques we will use are going to be decided during the process of the analysis, it is hard to tell exactly how we will visualize our results for now. This class is teaching us to quantify and compute seemingly unquantifiable and uncomputable features of art. In this case, with the assumption that color periods come from the artist’s emotional state, we are quantifying the emotional content that state dictates, which is, arguably, the most important aspect of an art piece. Therefore, in addition to pure computational analysis, we can also employ some subjective, personal analysis of each individual artist by trying to figure out the artist’s feelings and motivations over a color period.

## Data

(10 points) 

This section will describe your data and its origins. Each item should contain a name of the data source, a link to the source, and any necessary background information such as:
- What is your cultural data source? 
- When was it made? 
- Who created the works? 
- Is it digital native, or is it some kind of scan, recording, photo, etc., of an analog form? 

A fraction of Zdzislaw Beksinski's scanned works from wikiart. [His work] (https://www.wikiart.org/en/zdislav-beksinski/)
All of Beksinski's paintings, photos, and digital work were done between at least 1956-2009, his death. Since a majority of his works are undated, it is impossible to tell when each painting was done, but there are clear distinctions in his style that can be pinpointed. This is what we would like to examine in comparison to Picasso's Blue Period.


## Code

(20 points)

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- data acquisition/scraping
- cleaning
- analysis
- generating results. 

Link each of your notebooks or .py files within this section, and provide a brief explanation of what the code does. Reading this section we should have a sense of how to run your code.

[Cameron's Code] (code/Cameron S/Cameron S Beksinski Notebook)
This notebook walks through the scraping, cleaning, analysis and results of the Beksinski analysis portion of the midterm, as well as an attempt to test a classifier using the data gleaned from this sample of Beksinski's works.

## Results

(30 points) 

This section will contain links to documentation of your results. This can include figures, sound files, videos, bitmaps, as appropriate to your domain of analysis. Each result should include a brief textual description, and all should be listed below: 

- image files (`.jpg`, `.png` or whatever else is appropriate)
- audio files (`.wav`, `.mp3`)
- written text as `.pdf`

[brightness vs hue] (results/results-zdzislaw-beksinski/brightness_vs_hue.jpg)
Visualization of the mean brightness and the mean hue of each of the chosen Beksinski works.
[saturation vs hue] (results/results-zdzislaw-beksinski/saturation_vs_hue.jpg)
Visualization of the mean saturation and the mean hue of each of the chosen Beksinski works.
[entropy vs energy] (results/results-zdzislaw-beksinski/mean_entr vs mean_ener.jpg)
Visualization fo the mean entropy and the mean energy of each of Beksinski's works.
These visualizations combined show that there are distinct divides in the sample of Beksinski's works that were chosen. 
## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally relevant?
- How does your computational approach differ from the traditional art historical, musicological, manuel/subjective approach to analyzing your cultural subject? 
- How do you think the original artists/musicians would respond to this type of analysis? Would it change/inform their practice in some way?
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- In what future directions could you expand this work?

Observation shows that there are several, the main standouts being the black and white type, the predominantly orange type, the blue type, and periods that are greyer or somewhere in between. In Cameron's code, he attempted to train a classifier to identify orange and non-orange paintings, but the score was low. If a follow-up were to be planned, it'd probably be better to use a much larger sample. However, for this project we decided not to use all of them, as that would've been much too large.

Zdzislaw Beksinski's works are famous for their surreal, fantastical, almost post-apocalyptic style, and his influence can be seen across western media, especially in the horror genre, in which his works seem to best be described. However, Beksinski, being the eccentric he was, rarely dated or signed his paintings. For us, as data scientists, this presents a unique issue in that everything must be done relative to the rest of his paintings. Unlike Picasso, where we can accurately date periods that share style and color. So unlike Picasso, this is a situation wherein we cannot with certainty say that there is a Beksinski "Orange Period." One thing that can be said is that his paintings are uniquely gloomy in tone, their saturation and brightness clearly similar to one another, yet their colors can vary from a gloomy grey to a bright blue. Moreover, the paintings are also distinctly dynamic in their presentation. There was very little low entropic, low energy works. There were always vibrant colors to accompany the macabre imagery. 
If future statistics were to be done on these paintings, perhaps comparisons between these paintings and other macabre horror titans can be made, like the *Alien* franchise for example, whose iconic design for the *Alien* super predator matches the macabre themes of Beksinski's paintings to a T. 

## Team Roles

Provide an account of individual members and their efforts/contributions to the specific tasks you accomplished.
Cameron Shaw - wrote code for the Beksinski scraping and analysis, as well as worked on the write-up.

## Technical Notes and Dependencies

Any implementation details or notes we need to repeat your work. 
- Additional libraries you are using for this project
- Does this code require other pip packages, software, etc?
- Does this code need to run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts
