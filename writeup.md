


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 4.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>


Andrew Choi

[achoi284@usc.edu](mailto:achoi284@usc.edu)

CAIS++ Winter Project

I worked on two separate projects with similar machine learning procedures. For the first one, chihuahuas and muffins look very similar in images. So the program classifies the images into whether it’s a chihuahua or a muffin. The second one classifies images of a hand into its appropriate ASL Alphabet symbol that it is presenting.  

**Datasets:**


    Chihuahua and Muffin


    [https://www.kaggle.com/datasets/samuelcortinhas/muffin-vs-chihuahua-image-classification](https://www.kaggle.com/datasets/samuelcortinhas/muffin-vs-chihuahua-image-classification) 


    ASL Alphabet


    [https://www.kaggle.com/datasets/grassknoted/asl-alphabet](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) 

I directly downloaded the dataset from kaggle into google collab, unzipped the file and directly used it for the testing. Specifically for ASL Alphabet, the test folder didn’t have a subfolder with the alphabet but instead files of the images. Therefore, I just split the train data into test and train and used that for the classification.

**Training**:

	For both projects, I used transfer learning on a pretrained resnet18 model. I split the data into training data and testing data to train and validate each image batch processed using the resnet model. 

	Because of the sheer size of the data (the ASL data was 1GB), I limited the number of epochs to 3 for ASL and 5 for chihuahua. 

**Results:**

Chihuahua & Muffin:

	Model Accuracy



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")



    Results:



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


	**Final Accuracy: 99.49%**

ASL Alphabet:

	Accuracy:



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")


	Results:



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")



    **Final Accuracy: 92.52%**

**Discussion (only for ASL):**

	The dataset, model architecture, and training procedures all fit the task at hand well. The data was divided into folders of the alphabet/the value with train and test set, so I just directly added those data into the tensors to train them. But for the ASL classification, the runtime was too much so I had to limit the number of epochs but I would increase it for future time. Yes this can contribute to people using ASL hand signals via devices we build since it can recognize different hand signals. If I were to continue this project, my next step would be to potentially get data of different positions of the letters when the person moves because if this model was used in the real world, it would most likely involve movement from cameras. Also, I would try to get more than the alphabet and certain expressions that can be expressed by hand signals. 

	
