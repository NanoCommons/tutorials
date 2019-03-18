# ACEnano Knowledge Infrastructure Manual
**Last update**: 13 March 2019

**Authors**: Oana Florean, Maja Brajnik, Lucian Farcal [(Edelweiss Connect GmbH)](https://edelweissconnect.com/)

**Contact**: acenano@edelweissconnect.com

**Web access**: https://acenano.douglasconnect.com/

## Table of contents
[How do I access the knowledge infrastructure?](#How do I access the knowledge infrastructure?)


## How do I access the knowledge infrastructure?
The ACEnano knowledge infrastructure is freely available to anyone interested in accessing or uploading data (including protocols and experimental results) related to physicochemical characterisation of nanomaterials.

* *Under implementation*

## What are the main features of the knowledge infrastructure?
The ACEnano knowledge infrastructure (KI) is built using an open source software and includes multiple database instances (relational and non-rational (NoSQL) database) to optimally accommodate the requirements of the different data types (raw and processed data, summary results and protocols).
The features of the KI allows the users to:
* Create, store and share protocols on physicochemical characterisation of nanomaterials;
* Upload, store and share nanomaterials physicochemical characterisation data;
* Track the experimental results to the protocols used to generate the respective datasets.


## How do I add a new protocol?
The protocols database facilitates the access and sharing of methodologies applied in nanosafety. The methods are easy to browse and are linked to experimental datasets. This tool aims also to facilitate sharing of state of the art methods with the NanoEHS community and beyond.

After logging on at https://acenano.douglasconnect.com/ you can add a new protocol by following these steps:

1.Click the *Protocols* button from the top menu to open the *ACEnano Protocols* page which is the starting point of the protocols section. 

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/Intro.png">
  <b>Fig. 1 ACEnano intro page</b><br> 
  <br><br>
</p>

Fig. 1 *ACEnano intro* page

2.*ACEnano Protocols* page contains an explanatory paragraph and a scheme on the process of accessing and sharing the protocols, a red button *Add a new protocol* and the list of all added protocols until date labelled on *Protocol type*, *Protocol name* and *Posted*.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/ProtocolsPage.png">
  <b>Fig. 2. ACEnano Protocols page</b><br> 
  <br><br>
</p>

Fig. 2. *ACEnano Protocols* page

3.By clicking the button *Add a new protocol*, a new page is displayed (Fig. 3. Add a new protocol page), containing the description of the different type of protocols (in a questionnaire-like format) which can be added to the database:
  - **Sample Preparation Protocol**
  - **Measurement Protocol**
  - **Data Treatment Protocol**

Additional guidance and/or an examples are given to some of the fields in the questionnaire.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/AddNew.png">
  <b>Fig. 3. Adding a new protocol page</b><br> 
  <br><br>
</p>

Fig. 3. *Add a new protocol* page

4.For all the three protocols types, the first page of the protocol is approximately the same. It contains an explanation of the protocol parts and the questionnaire on *Part 1: General information*.

4.1.*Protocol name and description* area has the fields *Protocol original name*, *Version of this protocol*, *Variant of this protocol*, *Brief description*, *Long description*, *References* to be completed with free text and the dropdown lists *Development phase*, *Confidentiality*, *License* to be clicked for choosing an exclusive item.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/GenInfo.png">
  <b>Fig. Protocol name and description area</b><br> 
  <br><br>
</p>
 
Fig. *Protocol name and description* area
  
4.2.*Contacts* area contains text fields on *Name and email of contact person for the protocols*.
   
4.3.*Technique and Endpoints* area is different for each of the protocol types: 

4.3.1.For **Sample Preparation Protocol**, it contains a list box with multiple techniques, allowing multiple selection at a time, by holding Ctrl

4.3.2.For the **Measurement Protocol**, it contains a dropdown list on *Technique*, a list box *Endpoints*, allowing multiple selection at a time, by holding Ctrl and a dropdown list on *Phase*.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/Contacts_Technique.png">
  <b>Fig. Contacts area and Technique and Endpoints area</b><br> 
  <br><br>
</p>

4.3.3.For the **Data Treatment Protocol**, this part doesn't exist.
  
5.By pressing the red bottom *Continue to next step* at the end of the first page, the protocol chestionare continues with pages specific for each protocol type:

5.1.For **Sample Preparation Protocol**, the second page embodies *Part 2: Steps*, containing the *Step* box and the dropdown list of *Actions*. Steps can be deleted by selecting the checkbox *Delete this step* and extended by pressing the *+Add another step* button.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/Steps.png">
    <b>Fig. Page 2 of Sample Preparation Protocol</b><br>
  <br><br>
</p>

5.2.For the **Measurement Protocol**:

5.2.1.The second page embodies *Part 2: Equipment*:
- *Equipment* area,  with:  *Name*, *Model*, *Instrument type*, *Limit of detection upper*, *Limit of detection lower*, *Limit of       detection unit*, *Instrument settings and parameters* fields;
- *Possible datasets*area, with: *Axe*, *Units*  fields
- *Measurement quality parameters* area, with: *Parameter*, *Common setting* and  *Units* fields.

In each of these areas, the fields can be completed with free text, deleted by checking the delete boxes or extended by clicking the addition button. 

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/Equipment.png">
  <b>Fig. Equipment area from Part 2 of Measurement Protocol</b><br>
  <br><br>
</p>

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/PossibleDataSets.png">
  <b>Fig. Possible datasets area from Part 2 of Measurement Protocoll</b><br>
  <br><br>
</p>

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/MeasurementQualityParam.png">
  <b>Fig. Measurement quality parameters area from Part 2 of Measurement Protocol</b><br>
  <br><br>
</p>

5.2.2.By clicking the red button *Continue to the next step* the protocol questionnaire continues with another page. 

5.2.3.The third page embodies *Part 3: Steps*, containing the *Step* number box, *Name* and *Description* fields to be completed with    free text. Optionally, an image can be uploaded via *Chose file* in the *Image* box. Steps can be deleted by selecting the checkbox     *Delete this step* and extended by pressing the *+Add another step* button.

5.3. For **Data Treatment Protocol**, the second page, embodies *Part 2: Steps*, containing the *Step* number box, *Algorithm applied*, *Resulting data* and *Parameters* fields to be completed with free text.  Steps can be deleted by selecting the checkbox *Delete this step* and extended by pressing the *+Add another step* button.

6.By clicking  the red *Submit protocol* button at the bottom of the last page of the protocol questionnaire (second page for Sample **Preparation Protocol** and **Data Treatment Protocol** and third page for the **Measurement Protocol**), a page embodying the *Preview protocol* (Fig. Preview protocol page) will appear so the protocol can be proofread before submission. 

7.If everything it’s alright, the protocol can be committed by pressing the *Submit protocol* button. If corrections/modifications are needed, by pressing the *Make more changes* button, editing can be done in any part or area of the protocol by being redirected at *Part 1: General information* and moving towards the *Preview protocol* page.

<p align="center">
  <img src="https://github.com/NanoCommons/tutorials/blob/master/ACEnano%20manuals/Review.png">
  <b>Fig. Fig. Preview protocol page</b><br>
  <br><br>
</p>

8.After pressing the *Submit protocol* button from *Preview protocol* page, the new added protocol will appear on top of the *LATEST POSTS* list with the flag *protocol*,  a small description and the type of the protocol and the date when it was published(submitted).

## How do I create a new data workflow?
The data warehouse offers long-term storage of data produced by the nanosafety community. The data warehouse aims to support the data harmonisation and the implementation of FAIR principles towards the goal of generating a reference resource for nanomaterials risk assessment.
To achieve this goal, the user can select any of the data on samples and methods added into the protocols database, create and save the full workflow applied for the nanomaterials characterisation and link with the measurement results. This facilitates the tracking of results to the methodology, comparison of methods and results between different users or laboratories, support the round-robin experiments for method benchmarking and finally document all steps performed on a sample from the identification to the final results.


## How can I request support or suggest improvements of the platform?
For any inquiries regarding the content or functionalities of the Knowledge Infrastructure, You can contact us by email:
* Suggestions or technical issues: ACEnano team at Edelweiss Connect acenano@edelweissconnect.com
* For general support on protocols: Dr. Geert Cornelis, SLU geert.cornelis@slu.se
* For specific questions on procedures please contact the owners of the protocols
* Support on the dissemination activities: Daniel Fernandez-Poulussen, IDONIAL Daniel.Fernandez@idonial.com
