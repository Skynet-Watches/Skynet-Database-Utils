# Skynet Watches
![Logo](Logo-small.png)

## Inspiration
We were inspired to build Skynet Watches when we started looking into all the different ways people share their personal and identifying information. We recognized the possible applications in many industries, from retail to defence, and wanted to explore implementing a system to take advantage of this publically available data.

## What it does
Skynet Watches is a tightly integrated facial recognition system, based on Amazon Rekognition, coupled with custom infrastructure in order to leverage its full potential. By taking data from a variety of sources by a variety of methods, from automatically scraping social media to taking photos with a table, Skynet Watches builds a formidable database on its target users, in this case, Hack Poly participants. As such, it is capable of linking images of an individual to his or her identity.

## How we built it
![Diagram](Diagram.png)
Skynet Watches is built on Rekognition, storing all the metadata in a dynamoDB. We store the reference images in S3 in order to have the maxium scalability. In addition, we are leveraging CloudWatch and CloudTrail to get insight on what kind of API calls we are making and how we can  possibly improve by caching, or code refactoring.

## Challenges we ran into
Implementing an effective adaptive correlation filter that can leverage both Haar Classifier, and Camshift in order for us to be able to continue to track faces even after they have turned away from us.

Optimizing the client performance using multithreading turned out to be very challenging to get just right. This required many iterations before we finally landed on a good solution.


## Accomplishments that we're proud of

### Mark 
Making good progress on combining Haar Classifiers and Camshift in order to track people more effectively and minimize requests to our APIs. As well as writing the interface layers that power our frontend.

### James
I'm proud of creating a dynamic interface for our project using Python and Tkinter to reduce code complexity. Also, for efficiently linking data from the OpenCV component to the AWS interfaces to display meaningful data.

## What we learned

### Mark
Creating novel tracking algorithms that support many objects at once is hard to do in 24 hours.

### James
How to use Tk/Tkinter in Python to create attractive and scalable GUIs.

## What's next for Skynet Watches
We want to continue to explore what might be possible and non-evil among the many applications of this technology.
