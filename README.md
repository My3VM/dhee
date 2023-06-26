# CohortIQ
As conventional collaborative filtering methods become outdated, there is a critical necessity to extract context beyond the usual user behaviours in order to provide personalised recommendations to users. This challenge becomes more daunting as the user base and content repositories grow, making it increasingly difficult to generate personalised recommendations for each user that cover the entire content spectrum. This is where the concept of leveraging social intelligence emerges. By mining social intelligence within a natural context, it is possible to infer underlying crowd intelligence which can be harnessed to produce higher-quality results compared to relying solely on explicitly assigned topic tags.

#What it does
In a nutshell, this solution exploits user patterns to explore future patterns, leading to interesting yet serendipitous recommendation! The project analyses inherent patterns among community members and leverages this contextual information to generate customised recommendation summaries specific to each of the user segments. The emerging insights represent the inherent interest areas for the clusters which can benefit overall community by cross-referencing related topic areas and yield more meaningful, abstract ideas that better represent user communities. In essence, the goal of this project is to utilise GenAI to personalise content feeds for diverse user groups, taking into account their evolving preferences and trends on a large scale.

#How we built it
As an example, we utilised the MIND: Microsoft News Recommendation Dataset to showcase the methodology. The user representation was created by considering the content descriptions of their previous N news reads, while focusing on the latest N content access. This data was managed well inside Pinecone index along with its rich metadata. This data, presented in natural language format, was fed into Bertopic, which is powered by the OpenAI representation model. With the help of Bertopic, we were able to efficiently generate clusters and obtain coherent representation documents within those clusters.

The representation documents emerging from Bertopic cluster effectively captures the collective contextual representation of each cluster. This information is then fed back into the OpenAI model to generate inherent-abstract topics. These topics accurately reflect the areas of interest for each user segment, which can be leveraged to generate news digest recommendations at a large scale, tailored to the specific preferences of each cohort.

