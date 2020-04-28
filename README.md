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

## Code

(20 points)

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- data acquisition/scraping
- cleaning
- analysis
- generating results. 

Link each of your notebooks or .py files within this section, and provide a brief explanation of what the code does. Reading this section we should have a sense of how to run your code.

## Results

(30 points) 

This section will contain links to documentation of your results. This can include figures, sound files, videos, bitmaps, as appropriate to your domain of analysis. Each result should include a brief textual description, and all should be listed below: 

- image files (`.jpg`, `.png` or whatever else is appropriate)
- audio files (`.wav`, `.mp3`)
- written text as `.pdf`

## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally relevant?
- How does your computational approach differ from the traditional art historical, musicological, manuel/subjective approach to analyzing your cultural subject? 
- How do you think the original artists/musicians would respond to this type of analysis? Would it change/inform their practice in some way?
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- In what future directions could you expand this work?

## Team Roles

Provide an account of individual members and their efforts/contributions to the specific tasks you accomplished.

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
