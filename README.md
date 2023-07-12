# GSoC_2023_caMicroscope_Report
Progress report for GSoC 2023 caMicroscope Machine learning Training Assistant 

## Project Overview
To improve pathology data collection, caMicroscope has added specific tools for assisting with annotations and classifications. However, these tools require a pretrained model and the training workflow is difficult to use. The machine learning training assistant project aims to consolidate and improve the training workflow while also enhancing the user experience. This project may involve adding a microservice to enable training on a server and runtime analysis to determine the most useful information at a given time.

## Milestones

## Timeline
### Community bonding period (May 5th - May 28th)
During community bonding period, I have some meeting with caMicroscope memtors and an one on one meeting with my main mentor Nanli. I also get to know more about caMicroscope organization. 

My work would base on existing code on caMicroscope (Frontend) and Caracal (Backend). I start with reading related code and try to test features. I also try to change some part of the code to see how it would effect the visual and performance.

### Week 1 (May 29th - June 4th)
* Brainstorm ideas to improve user experience on caMicroscope specially take advantage of existing model to create an semi-automatic annotation platform.
* Design UI for `semi-automatic annotation` feature
<img width="470" alt="" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/3cbab273-582b-43ff-b0b6-565d40d15a20">

<img width="492" alt="" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/5485c02d-113f-482a-b2d1-b7c878e0afa2">

### Week 2 (June 5th - June 11th)
* Implementing `annotation edit` feature
+ Draw edit points corresponding with annotation shape (Polygon)
+ Redraw annotation shape when user change position of the edit points

<img width="526" alt="Screenshot 2023-06-19 at 1 35 17" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/9619ae86-ec81-4432-888d-97ad3cbef9fb">

### Week 3 (June 12th - June 18th)
* Continue to implement `annotation edit` feature
+ Connect with backend to save annotation in database after edit completion
+ Create `annotation edit` feature for other type of annotation (Brush, Point)

<img width="485" alt="Screenshot 2023-06-19 at 1 39 59" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/eaa15972-4fa0-4c9b-a410-e0d7a029442c">
<img width="278" alt="Screenshot 2023-06-19 at 1 40 20" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/f0255046-a151-4f04-b002-78b9cf288c82">

### Week 4 (June 19th - June 25th)
* Create Annotation Assistant UI which integrate segmentation model into view page in right side of screen. It can be toggled when click on `preset-label` button
* UI incude
+ Model management (Add model, enable annotation assistant, choose model, choose pixel scale and show model info)
+ Assistant Mode (Draw, Click, ROI) (The drawing method which annotation assistant can support)
+ Assistant Setting (Radius, Threshold, Roughness) (Model parameter which could be change when draw mode change)

<img width="526" alt="Screenshot 2023-06-26 at 19 28 56" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/a8087819-b021-4861-ac46-84276c699a43">

### Week 5 (June 26th - July 2nd)
* Implement prototype for machine learning annotation by drawing
+ Working principle:
  - Processing user drawing input and model generated mask to predict the best fit boundary

<img width="526" alt="Screenshot 2023-07-12 at 19 28 49" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/cfdcdd7c-a4b1-4930-9e68-88ac3382906d">

### Week 6 (July 3rd - July 9th)
* Integrate machine learning annotation by drawing with Machine learning Assistant panel
* Add two new parameter ```Kernel Size``` and ```Iteration``` to allow user choosing their separation level
* Add two regions for ```Processed Image``` and ```Model predicted image```

<img width="251" alt="Screenshot 2023-07-12 at 19 30 41" src="https://github.com/BryanGsep/GSoC_2023_caMicroscope_Report/assets/77573775/41150eb1-8461-4cf5-aaf9-bba1c7259f9c">

