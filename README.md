# Stellar Characteristics in the Milky Way: Unravelling Galactic Mysteries ReadME

## Title: **Stellar Characteristics in the Milky Way: Unravelling Galactic Mysteries**
![Description of the image](https://github.com/J4smith0601/Stellar-Characteristics-in-the-Milky-Way-Unraveling-Galactic-Mysteries/raw/main/Stellar%20Characteristics%20in%20the%20Milky%20Way%20Unraveling%20Galactic%20Mysteries%20.png)

---

## Project Overview:

This project, undertaken as the first assignment for the Data Science & AI course with the Institute of Data and Auckland University of Technology, focuses on analysing the intrinsic properties of stars within the Milky Way using data sourced from the AT-HYG database. The goal was to translate a broad astronomical problem into a data science problem by selecting and processing a relevant dataset.**  The analysis began by identifying and excluding 60,745 entries with missing positional and distance data, resulting in a final sample of 2,491,418 stars. Key features such as absolute magnitude, luminosity, mass, radius, and temperature were engineered from the dataset. Initial descriptive statistics suggested potential skewness in the data, which was further examined using the Shapiro-Wilk test along with measures of skewness and kurtosis. Despite Box-Cox transformations aimed at normalising the data, non-normal distributions persisted across all variables.  Visual inspections through histograms, Q-Q plots, and box plots corroborated these findings. Additionally, a bar chart of spectral class frequencies indicated a distribution aligned with known astronomical patterns, supporting the dataset’s representativeness. Correlation analysis uncovered significant relationships among intrinsic stellar properties, highlighting potential avenues for further research.  The spatial distribution of these properties across the Milky Way was also explored, providing insights into their variability within the galaxy.  **Overall, this exploratory data analysis offers a robust foundation for understanding the distribution and interrelationships of stellar properties, setting the stage for future research into stellar dynamics and galactic structure. The assignment demonstrated the application of data wrangling, feature engineering, and exploratory data analysis techniques acquired throughout the course.

--- 

## Technologies Used

- **SQL**: Utilised for querying and managing the dataset.
- **Python**: The primary programming language used for data analysis and processing.
  - **sqlite3**: Used to import star data from the SQLite database.
  - **Pandas**: Applied for data manipulation and analysis.
  - **NumPy**: Employed for numerical operations and array handling.
  - **inflect**: Used for converting numbers into words for improved readability and interpretation.
  - **Seaborn**: Leveraged for advanced data visualizations and statistical plotting.
  - **Matplotlib**: Utilised for creating plots and visualizations.
  - **SciPy**: Applied for statistical calculations and normality checks.
    - **scipy.stats**: For various statistical functions and normality testing.
    - **skew**: Measures the skewness of the data.
    - **kurtosis**: Measures the kurtosis of the data.
    - **shapiro**: Performs the Shapiro-Wilk test for normality.
    - **norm**: Provides normal distribution functions.
    - **probplot**: Creates quantile-quantile plots.
    - **boxcox**: Used for Box-Cox transformations to stabilize variance and achieve normality.
  - **math**: Applied for mathematical calculations related to astronomical computations.
- **Jupyter Notebook**: For interactive analysis and documenting the process.
- **VS Code**: The IDE used for coding and managing the project.
- **Git**: For version control and tracking changes.
- **GitHub**: Hosted the repository and supported collaboration.

--- 

## Installation Instructions

To run this project locally, follow these steps:

**1. Clone the Repository:**
Open a terminal or command prompt and run the following command to clone the repository:
git clone (https://github.com/j4smith0601/Stellar-Characteristics-in-the-Milky-Way-Unraveling-Galactic-Mysteries.git)]

**2. Navigate to the Project Directory:**
Change your directory to the project folder:
cd [Stellar-Characteristics-in-the-Milky-Way-Unraveling-Galactic-Mysteries]

**3. Install Dependencies:**
Ensure you have Python installed on your system. Then, install the required libraries using pip.
sqlite3
pandas
numpy
inflect
seaborn
matplotlib
scipy

**4. Set Up SQLite Database:**
- Download the AT-HYG.db file from the dataset provided database file.
- Open SQLite Studio.
- Go to Database > Add Database and select the AT-HYG.db file you downloaded.
- Ensure the database is properly loaded and accessible in SQLite Studio.

**4. Run the Jupyter Notebook:**
- Launch Jupyter Notebook and run all

**5. Verify Installation:**
To verify that the dependencies are correctly installed, you can run a Python script or open a Jupyter Notebook and import the libraries to ensure they are available.

---

## Usage

This project demonstrates the exploratory data analysis (EDA) capabilities acquired during the Data Science & AI course. It is designed to showcase my skills in data manipulation, statistical analysis, and visualization to potential stakeholders, future employers, and other interested parties.

---

## Results and Analysis 

### Key Findings from Exploratory Data Analysis

The sample data on the position and apparent magnitude of stars was acquired from the AT-HYG database. Initially, a relatively small number of null values were identified, specifically 60,745 stars with missing data related to position and distance variables. These missing variables could not be calculated from the available data, and imputing them using averages or similar methods would impose bias. Examination of their distribution among the constellations in the database suggested that the deletion of these entries would not impact the representativeness of the data. After handling the missing data, the final sample size was 2,491,418 stars.

Key variables such as absolute magnitude, luminosity, mass, radius, and temperature were calculated across the database. Descriptive statistics for these variables revealed significant differences between the mean ($\mu$) and median values ($\tilde{M}$), indicating potential skewness. For instance, the temperature had a mean of 8032.93, a standard deviation ($\sigma$) of 1758.67, and a median of 7827.61, while luminosity had a mean of 41.45, a standard deviation of 2384.28, and a median of 9.43. Similar patterns were observed for mass ($\mu$ = 2.12, $\sigma$ = 1.02, $\tilde{M}$ = 1.90), radius ($\mu$ = 1.79, $\sigma$ = 0.68, $\tilde{M}$ = 1.67), and absolute magnitude ($\mu$ = 2.38, $\sigma$ = 2.39, $\tilde{M}$ = 2.39).

Skewness ($\gamma_1$), kurtosis ($\gamma_2$), and Shapiro-Wilk ($ W $) tests were conducted to assess normality, and the results confirmed significantly non-normal distributions for all variables. For example, temperature had a skewness of 2.11, kurtosis of 8.54, and a Shapiro-Wilk statistic of 0.82 (p < 0.001). Visual inspection using histograms, Q-Q plots, and box plots further supported these findings.

Box-Cox transformations were attempted to reduce skewness and kurtosis. Although these transformations significantly reduced both skewness and kurtosis, all variables remained significantly non-normally distributed. For example, the transformed temperature had a mean of 16.36, a standard deviation of 0.65, and a median of 16.34, while the transformed luminosity had a mean of 2.33, a standard deviation of 1.66, and a median of 2.29.

The frequency distribution of spectral classes was analysed using a bar chart. The distribution of this categorical variable matched expectations, reflecting the inherent complexities and natural variation of stellar populations across the cosmos. The most common spectral classes were A (1,085,220 stars) and F (835,044 stars), followed by B (316,371 stars), G (194,447 stars), K (57,507 stars), M (2,811 stars), and O (18 stars).

Correlation analysis of the key variables revealed important relationships among them. A strong positive correlation was found between mass and luminosity, suggesting that as a star’s mass increases, its luminosity also tends to increase. Additionally, the spatial distribution of the key intrinsic properties was analysed across this stellar population. The findings suggested distinct patterns in the distribution of stars, with certain regions showing higher densities, reflecting the structure of the Milky Way.

In summary, the exploratory data analysis revealed valuable insights into the distribution and relationships among key stellar properties in the AT-HYG database. Despite the challenges posed by non-normal distributions, the analysis highlighted the complex and varied nature of stellar populations. The findings from the spectral class distribution and spatial analysis align with known astronomical phenomena, reinforcing the representativeness and reliability of the dataset.

---

## License

This project is not licensed under any specific license. You are free to use, modify, and distribute this project as you see fit. However, please note that this project is intended for personal use and portfolio showcasing purposes. If you share or distribute this project, please ensure that any derivative works or modifications adhere to the same principles of personal use and respect for the original work.

---

## Acknowledgements

- The original dataset used in this project was obtained from the HYG Database on GitHub. This comprehensive stellar data provided the foundation for the analysis performed in this project. I appreciate the efforts of the contributors to the HYG Database for making this valuable resource available.
- Special thanks to Laks Balasubramanian and the Data Science & AI course team at the Institute of Data and Auckland University of Technology for their guidance and support throughout this assignment.
- I would also like to acknowledge the use of various Python libraries, including Pandas, NumPy, Seaborn, and Matplotlib, which were instrumental in data manipulation and visualization.
- No external funding or grants were received for this project.

---

### Data Source

The original dataset used in this project was obtained from the HYG Database on GitHub. This database provides comprehensive stellar data, which served as the foundation for the analysis conducted in this project.

You can visit the HYG Database repository for more information about the data, including its structure and additional details.

---

## Contact Information

For feedback, networking, or inquiries related to this project, please feel free to reach out:

- LinkedIn: https://www.linkedin.com/in/jasmith0601/
- Email: James.smith@andersmith.co.nz

You can connect with me via LinkedIn or email to discuss the project, explore collaboration opportunities, or provide feedback.
