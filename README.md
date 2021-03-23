
# Seeing your Heart through your Eyes: Predicting Myocardial Infarction using Retinal Images and Demographic Data

This is the project web for the study titled "Seeing your Heart through your Eyes: Predicting Myocardial Infarction using Retinal Images and Demographic Data". This is study is under review in the journal Nature Machine Intelligence.


----------------

## System Requirements:

### OS Requirements

The package development version is tested on *Linux* operating systems. The developmental version of the package has been tested on the following systems:

Linux: CentOS Linux 7 and Ubuntu 

### Package dependencies

We used Python 3.6.5. File **requirements.txt** contains the list of python libraries/packages used to train our approach.

### Weights

The weights of the trained models (~5GB) could be download from this [link](https://emckclac-my.sharepoint.com/:f:/g/personal/k2039747_kcl_ac_uk/EqjWo8c37A1LvuVGJcF9XhwBoh5d-7Sy-vPsewBaA3jkeQ?e=0d0d0H).


## Steps for external validation


- As the first step, please create a Python virtual environment and then install all the libraries listed in **requirements.txt** file using the command "pip install -r requirements.txt". This will take about 10 mins to finish.

- Secondly, modify the dataloader file ('dataloader/MM_loader_4_test_EXTERNAL.py') according to the data organization you have. Then, create the input file (.csv file) following the example located in './input_data_EXTERNAL/ids/ids_metadata_EXTERNAL.csv'. 

- For this toy example, I used a small part (100 images) of the DR Kaggle dataset and I randomly draw metadata values for each subject: ID,sex,dbpa,sbpa,ss,ads,bmi,age,hba1c,chol,glucose


You can use the script **test_dataLoader_MM_4_test_EXTERNAL.py** to test your dataloader.


I uploaded the weights of a system trained with the following metadat: gender ('sex'), [smoking status](https://biobank.ndph.ox.ac.uk/showcase/field.cgi?id=20116) ('ss'), [drinking status](https://biobank.ndph.ox.ac.uk/showcase/field.cgi?id=1558) ('ads'), body mass index ('bmi'), age ('age'), [hba1c](https://biobank.ndph.ox.ac.uk/showcase/field.cgi?id=30750), diastolic blood pressure ('dbpa'), systolic blood pressure ('sbpa'), [cholesterol](https://biobank.ndph.ox.ac.uk/showcase/field.cgi?id=23400) ('chol') and glucose ('glucose').


- Thirdly, you should download the [weights](https://emckclac-my.sharepoint.com/:f:/g/personal/k2039747_kcl_ac_uk/EqjWo8c37A1LvuVGJcF9XhwBoh5d-7Sy-vPsewBaA3jkeQ?e=0d0d0H) inside the main folder in a folder called 'results'.


- Finally, you should run the script **main_EXTERNAL.py** to test on the retinal images.



If you are having an issue that you believe to be tied to software versioning issues, please drop us an [Issue](https://github.com/diazandr3s/MI_pred_mcvae_ukbb/issues) or send us an email to andres.diaz-pinto@kcl.ac.uk

 
----------------

Update log (Year.Month.Day):

- 20.08.14: Code released.
- 20.09.15: Network weights uploaded. Article under review.
- 21.22.03: Creaated a branch for external validation

