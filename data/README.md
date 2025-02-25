
# Disease Prevalence Data by Sex, Age, Year, and ICD Code (1997-2014)

## Dataset Description
This dataset contains 135,708 hospital records in Austria from 1997 to 2014 displaying disease prevalence categorized by sex, age group, year, and ICD code. It includes records from various years, detailing the prevalence rate (`p`) of different diseases within specific demographic groups.

## Data Dictionary

| Column Name | Data Type | Description |
|-------------|----------|-------------|
| `sex`       | String   | The gender category of the population (`Male` or `Female`). |
| `Age_Group` | String   | The age group category (e.g., `0-9`, `10-19`, etc.). |
| `year`      | Integer  | The year of data collection (e.g., `2003`, `2004`). |
| `icd_code`  | String   | The ICD (International Classification of Diseases) code associated with a specific disease. |
| `p`         | Float    | The prevalence rate of the disease within the given demographic group. |

## Source
This dataset is sourced from [figshare](https://figshare.com/articles/dataset/Comorbidity_Networks_From_Population-Wide_Health_Data_Aggregated_Data_of_8_9M_Hospital_Patients_1997-2014_/27102553?file=52015403).

### How to obtain:

After getting into the figshare page, under the title "Comorbidity Networks From Population-Wide Health Data: Aggregated Data of 8.9M Hospital Patients (1997-2014)" there is a `Download(203.1 MB)` button. Click that button, the `Data.zip` file will automatically start downloading (Fig. 1).
![The Figshare Page](https://github.com/user-attachments/assets/6c72e983-84fa-47fd-8c75-465acead4beb)

After finishing downloading, open the `Data.zip` file, click the `Data` folder, then enter the `1.Prevalence` folder, in which the `Prevalence_Sex_Age_Year_ICD.csv` file is the dataset used.
![The Location of Dataset inside Folder](https://github.com/user-attachments/assets/5f6b379f-f6a3-48ed-8ab7-d483638acb9c)

## Purpose
This dataset is used to analyze the evolution of comorbidity networks over 1997-2014 in research conducted by the GitHub owner.

## Useage
Except for the usage in Purpose, this dataset can also be used to determine disease prevalence trends across different demographics over time. It is particularly useful for epidemiological studies and healthcare policy analysis.

## License
This dataset is provided for research and educational purposes.

## Contact
For any questions or further details, please reach out to the dataset provider.

## Ciation
Dervic, Elma (2025). Comorbidity Networks From Population-Wide Health Data: Aggregated Data of 8.9M Hospital Patients (1997-2014). figshare. Dataset. https://doi.org/10.6084/m9.figshare.27102553.v2
