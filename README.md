# Multimodal dataset of potentially offensive comments and images

In order to study online hate speech, the availability of datasets containing the linguistic
phenomena of interest are of crucial importance.
However, when it comes to specific target groups, for example teenagers, collecting such data
may be problematic due to issues with consent and privacy restrictions.
Furthermore, while text-only datasets of this kind have been widely created and shared, limitations
set by image-based social media platforms like Instagram make it difficult for researchers to
with multimodal hate speech data.
We therefore developed a multimodal dataset of images and potentially offensive comments in Italian,
created during awareness-raising activities in classes by students between 15 and 18 years old.
The dataset was created using the CREENDER tool (Palmero Aprosio et al., 2020).

Images randomly collected from the web were displayed to students, with a prompt asking "If you saw
this picture on Instagram, would you make fun of the person who posted it?". If yes, they had to
add a comment and select a category explaining the reason for the comment. The available categories
were Body, Clothing, Pose, Facial expression, Location, Activity, Other. The same images were displayed
several times so to collect multiple judgements.
Overall, 17,912 images have been judged at least once by the students. For 1,018 of them, at least 
an offensive comment has been written during the annotation sessions. Overall, the number of comments 
in the dataset is 1,135, which is higher than the number of pictures with a comment because the same 
image may be commented more than once by different students.
Since the comments were collected with the written consent of parents and teachers, they can be freely
used for research purposes, without the ethical implications that would derive from using real data 
posted by teenage users. The images, instead, are released as a ResNet-18 neural network trained on 
ImageNet

## Format

The dataset consists in a unique json file containing an array of records, each of them containing:

* comments: a list of annotations, where annotation is a value between 0 and 100, and comment is
  the text inserted by the user.
  * 0 - None
  * 1 - Body
  * 2 - Clothing
  * 3 - Pose
  * 4 - Facial expression
  * 5 - Location
  * 6 - Activity
  * 100 - Other

* vector: a list of 512 float numbers representing the picture, using ResNet-18 network pre-trained
  on ImageNet as the image encoder.

## Publications
Stefano Menini, Alessio Palmero Aprosio and Sara Tonelli. A Multimodal Dataset of Images and Text to Study Abusive Language. In Proceedings of the Seventh Italian Conference on Computational Linguistics (CLiC-it 2020), Bologna, Italy
