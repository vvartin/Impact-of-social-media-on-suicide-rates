# Impact of social media on suicide rates

## Description
This project explores whether increase in social media usage has impact on number of suicides via analysis of correlation of number of Facebook and Twitter users with the number of suicides. 

## Installation
No installation of special software is necessary but `python3`, `jupyter-notebook` and some additional non standard python modules - `pandas, matplotlib` - are necessary. In case the project is not runnable please refer to the exact versions in `documentation/dependencies-and-requirements.txt` for reference.

## Usage

### Steps to execute the experiment
* run the entire code/preprocess.ipnyb notebook to produce a preprocessed dataset for analysis along with stepwise intermediate datasets
* run the code/analysis.ipnyb notebook to produce the visualizations and verify the outcome of the experiment

* the corresponding produced data can also be found in a separate repository: https://github.com/vvartin/Impact-of-social-media-on-suicide-rates-results

To facilitate the usage additional project information might be necessary.

### Folder structure
* code/ - contains all code to reproduce the results
	* code/preprocess.ipnyb - takes raw datasets, prepares and merges them for analysis
	* code/analysis.ipnyb - consumes the preprocessed dataset and creates figures
	* code/provenance.ipnyb - validates the 
* data/ - contains all of the datasets both input and produced
	* input/ - contains the raw input datasets
	* produced/ - contains the datasets created by the code
		* provenance/ - contains intermediate datasets that can be used to verify the correctness of operations
			* reference/ - contains reference intermediate outputs to compare against
		* final/ - contains the final merged dataset used in analysis 
		* figures/ - contains produced figures
* documentation/ - contains metedata regarding the produced outputs, author, licencing
	* documentation/metadata.xml - authors, basic description, licencing, time of execution and others
	* documentation/output-description.txt - explanation of the produced files with regards to axis or newly produced columns
	* documentation/dependencies-and-requirements.txt - contains the list of packages required to run the experiment with versions.

### Naming convention
A *-* separator was chosen in place of spaces to facilitate command line interactions.

#### Intermediate datasets
- For produced intermediate datasets is as follows: \<dataset-name\>-\<step\>--\<timestamp\>
 	* name of the dataset the output is based on
	* step - the point at which the dataset was archived (see code/analysis.ipnyb for more details)
	* timestamp - timestamp in form DD-MM-YYYY-HHMMSS

#### Figures
- For figures the naming convention is as follows: \<figure-type\>--\<timestamp\>
	* figure-type - the type of the figure, descriptive name what the figure contains


### Divergent output troubleshooting 
* in case the output does not match code/provenance.ipnyb can be used to verify your outputs against reference outputs produced by the researchers. This validations can be done stepwise to discover the precise point where the datasets diverged.

## Output dataset
The output dataset is located in data/produced/final/merged-preprocessed.csv and is always overridden with the last run. A reference output dataset produced by the researchers is also located in data/produced/provenance/reference/merged-preprocessed.csv

## Credits
* WHO data export (https://apps.who.int/gho/athena/api/GHO/SDGSUICIDE.csv) was used bound by the following poilcy: https://www.who.int/about/who-we-are/publishing-policies/data-policy

* Kaggle dataset regarding social media usage was used (https://www.kaggle.com/margarethamartinez/socialmedia2021) with additional acknowledgements of the original sources necessary:
	* Acknowledgements:
		* Facebook: https://www.statista.com/statistics/264810/number-of-monthly-active-facebook-users-worldwide/
		* Twitter: https://investor.twitterinc.com/home/default.aspx
		* Instagram: https://investor.fb.com/home/default.aspx

## License
The code and the produced data is lincenced under CC BY-SA-NC licence (see LICENCE file for further information)
