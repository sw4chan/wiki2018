Multiple trials went underway for the growth of J2T in knockout MetE media to definitively confirm that the predicted results occured in regards to NCM/J2T growth. As the goal of the experiment was to assure that there was no “leaking” of methionine from the J2T cells when stimulated with methionine production, the following test matrix was performed:


Test Tube #
Control
Components
Results
1
Experimental
→ M9 Dropout with NCM removed (2 mL)
→ Added JT2 (25 uL)
→ KM (2 uL)
No growth
2
Positive
→ M9 Dropout with NCM removed (2 mL)
→ Stock culture NCM (2 uL)
Minor growth*
3
Positive
→ M9 Dropout with NCM removed (2 mL)
→ Added JT2 (25 uL)
→ KM(2 uL)
→ MetE (100 uL)
Growth
4
Negative
→ M9 Dropout with NCM removed (approx. 2 mL)
→ KM (2 uL)
No growth
5
Negative
→ Stock M9 Dropout (2 mL)
→ KM (2 uL)
→ MetE (100 uL)
No growth
6
Negative
→ Stock M9 Dropout (2 mL)
→ Added JT2 (25 uL)
→ KM (2 uL)
No growth
7
Positive
→ Stock M9 Dropout (2 mL)
→ Added JT2 (25 uL)
→ KM (2 uL)
→ MetE (100 uL) 
Growth

//will figure out how to format this table soon

In this chart, a negative control refers to an experiment where there was an expectation that there should be no bacterial growth as per our hypothesis, and a positive control denotes an experiment where there should have been growth expected.

As can be seen from the chart, the experimental trial, in which the NCM strain was grown and removed from the methionine knockout media, had no growth once J2T was introduced into it. This was a positive result as this suggested that there was little or no “leaking” of methionine produced by the NCM during growth into the media, and thus the J2T did not have any means to grow. 

The minor growth of NCM as a positive in control in trial 2 was expected, and was done to confirm that there would be no adverse factors from the removal of NCM that were causing the introduced J2T to not be able to grow, and that the composition of the media was static.

Trial 3 showed with the repliaction of expirimental conditions and the addition of MetE that the reason that the growth was not happening in exsperimental conditions was in fact the lack of methionine in the M9 media. This showed growth as expected.

Trial 4 indicated no growth as expected. This was carried out, with the removal of the NCM and addition of the antibiotic, to confirm that all the bacteria was being taken out and that no other bacterial contamination was what was being seen in the positive control tests that had reported growth.

Trial 5 similarly was carried out with stock M9 to assure no environmental contamination was in the media from the beginning, especially bacteria that required external methionine to grow.

Trial 6 was carried out as a negative control to assure that the stock media itself was not contaminated with any nutrients that could be used by the JT2 to grow. This was important as it is possible that trace amounts could have been consumed in the other trials by the NCM bacteria and thus were not reflected in the experimental trial.  

Finally, the 7th trial indicated that the JT2 strain that was in this bacteria was healthy and could grow in the desired conditions within the M9 media, with the methionine and the KM from stock solution.

# ROBOT

## Initial Experiment
Having determined the utility of an automated sampling system, the team first set out to confirm whether or not cells with different levels of GFP expressed could be visually distinguished when exposed to a ~488 nm light source. To this end, a light source with a peak emission at 488 nm and a light filter capable of letting green light but not blue light pass through was borrowed from the Reed lab at the University of Waterloo.

Cells (specifically BW 29655 E. coli) expressing GFP under the CcaR promoter were grown to an OD of ~1 under both red and green light in complete M9. Unfortunately fluorescence measurements were not taken under the flow cytometer, but for the record the cells grown under red light were white while those grown under green light were visibly green. Upon shining blue light on the cells and taking a picture through the filter, the following image was obtained:

![alt text](http://2018.igem.org/wiki/images/a/a4/T--Waterloo--July18_initialFluorescenceCheck.jpg)

The container on the right was the one grown under green light, and it is very clearly distinguishable from the container on the right.

## Box Design and Test with Photodiode

## Quantification Test with Camera
After the unclear result of the test with the original box apparatus, it was determined that the test using the camera should be redone in a more quantitative manner. Similarly to the initial experiment, E. coli (this time JT2 containing GFP under the CcaR promoter) were grown up to an OD of ~0.6 in complete M9. Two samples were grown under green light, and two under red light.

The tubes were arranged in a row in front of an iPhone camera, which had a light filter in front of it that blocked out green light. The tubes were placed in two alternate arrangements, and a movie was taken of the blue LED being passed behind them. See below for one of the movies taken.

<video width="100%" height="480" controls> 
<source src="http://2018.igem.org/wiki/images/9/97/T--Waterloo--August21_robotsExp1.mov" type="video/mp4"> 
</video>

As one can see (especially when looking at the bottoms of the vials), the first and third vials from the left are brighter. These were the vials grown under green light, and hence having more GFP. Screenshots of the vials were taken as the light was directly behind them, and the images were cropped down to just the vial (see below for an example cropped image).

![alt text](http://2018.igem.org/wiki/images/1/19/T--Waterloo--August21_Arrangement1Vial1.jpg)

These images were then fed into a Python program that broke them down into their RGB values. The red, green, and blue values of each pixel in each image were taken and averaged. Since some blue light still made it through the filter, average blue values for the images could not be used to distinguish the samples. Additionally, the green values were informative but still relatively in each image, mostly because a strong blue light actually emits some green light as well. However, examining the average red values made the cells grown under red and green light easily distinguishable.

This led the team to conclude that our approach for distinguishing fluorescent and non-fluorescent cells was valid, and the failure of the initial box design was due to poor placement and control of the position of our photodiode, sample vial, and LED. We thus set out to find the optimal arrangement and implement that into future designs.

For the full code of the Python program, see:
https://github.com/igem-waterloo/uwaterloo-igem-2018/blob/master/models/image/greenFluorescenceQuantifier.py
For the full experimental protocol, see the online lab book (pages 80 and 81).

## Optimization Test with Camera

## Second Design and Future Experiments


