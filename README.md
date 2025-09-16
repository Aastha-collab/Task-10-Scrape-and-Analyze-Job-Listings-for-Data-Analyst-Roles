# Task-10-Scrape-and-Analyze-Job-Listings-for-Data-Analyst-Roles

###  **Project Summary**

In this project, I built a Python script to scrape **internship data from Internshala** for Data Analyst roles. The goal was to extract information such as job titles, companies, locations, salaries, and required skills, then analyze and visualize this data.

The project also focused on handling real-world scenarios like missing data and ensuring that the analysis only runs when data is available.

---

###  **Key Features**

* - **Scraping job listings** from Internshala using `requests` and `BeautifulSoup`.
* - **Handling missing or incomplete data** gracefully using error handling and checks.
* - **Checking if the dataset is empty** before proceeding with analysis or visualization.
* - **Extracting insights** such as the total number of internships, top locations, and most in-demand skills.
* - **Visualizing data** using bar and pie charts to make insights easier to interpret.

---

###  **Handling Empty DataFrames**

While scraping, it’s common to encounter situations where data may not be available or correctly loaded from the website. In this project:

* The script first verifies whether job listings exist on the page.

* If no data is found, the script outputs a message like:

  ```
  Found 41 internships on the page!
  ```

* After loading the data into a pandas DataFrame, it checks if the DataFrame is empty using:

  ```python
  if df.empty:
      print("No internship data available.")
  ```

* This prevents errors from trying to analyze or plot data that doesn’t exist and ensures that the script runs smoothly without interruptions.

---

###  **Insights Extracted**

* - **Total internships found:** 41 internships were listed on the page.
* - **Top locations:** The script counts and displays the most frequent job locations.
* - **Top skills:** By aggregating skills across all internships, it highlights the most in-demand expertise.

These insights are helpful for understanding trends in internship offerings and identifying areas where more preparation or upskilling is required.

---

###  **Technologies Used**

* **Python** – For scripting and automation.
* **requests & BeautifulSoup** – For web scraping.
* **pandas** – For data manipulation and storage.
* **matplotlib** – For creating meaningful visualizations.
* **Error Handling** – To avoid crashes when data is missing.

---

###  **Challenges & Solutions**

| Challenge                             | Solution                                                                      |
| ------------------------------------- | ----------------------------------------------------------------------------- |
| Some internships had missing details  | Used `try-except` blocks to handle missing information gracefully             |
| The page structure might change       | Used flexible parsing methods and verified data before use                    |
| Empty datasets causing errors         | Added checks before performing analysis or plotting                           |
| Avoiding being blocked by the website | Added headers and request delays (`time.sleep`) to mimic normal user behavior |

---

###  **Conclusion**

This project demonstrates how to build a robust web scraping pipeline that handles real-world complexities like missing data and incomplete entries. By ensuring that analyses only proceed when valid data is present, the script remains reliable and user-friendly. The insights drawn from the data provide actionable information for job seekers and recruiters alike.

---
