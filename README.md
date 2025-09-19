

# DBT Project – End-to-End Implementation

This repository is a hands-on implementation of what I’ve learned while working with **DBT (Data Build Tool)**. I explored and practiced core DBT concepts including models, seeds, snapshots, tests, macros, and even CI/CD deployment. Everything was done locally using **VS Code**, and this project reflects my understanding of building a proper DBT pipeline from scratch.

##  What I Learned & Implemented

Here’s a summary of the topics I worked through:

* DBT Core – Installation and basic commands
* Setting up the environment in **VS Code**
* DBT Project Structure
* Connecting DBT with **Databricks** using the DBT-Databricks plugin
* DBT Sources – Defining and using source tables
* DBT Models – Building transformation logic in modular SQL files
* DBT Seeds – Loading CSV files as source tables
* DBT Snapshots – Handling SCD Type-2 changes
* DBT Tests – Built-in and custom tests for data validation
* Jinja & Macros – Dynamic SQL and reusable logic
* Deployment – CI/CD setup for automated DBT runs

---

##  Tech Stack

* **DBT Core**
* **Databricks** (for warehouse connection)
* **VS Code** (for development)
* **GitHub** (for version control & CI/CD)
* **Jinja** (templating in SQL)

---

## 🗂️ Folder Structure

```bash
dbt_project/
│
├── models/            # All transformation logic
│   ├── staging/       # Raw to staging
│   └── marts/         # Final transformed models
│
├── seeds/             # CSV files used as seed data
│
├── snapshots/         # Snapshot logic (SCD Type-2)
│
├── macros/            # Jinja macros for reusable SQL
│
├── tests/             # Custom test SQL files
│
├── dbt_project.yml    # Main config file
└── README.md


## Running the Project

1. **Clone the repo**

   ```bash
   git clone https://github.com/Maruthireddy77/dbt-analytics-pipeline
   cd DBT_Practice_Project


2. **Install DBT**

   ```bash
   pip install dbt
   ```

3. **Configure your profile**
   Update your `~/.dbt/profiles.yml` file with the Databricks credentials or whichever data warehouse you’re using.

4. **Run DBT commands**

   ```bash
   dbt seed       # Load CSVs
   dbt run        # Build models
   dbt test       # Run tests
   dbt snapshot   # Capture historical changes
   ```

---

## Highlights

* Used **DBT Snapshots** to manage historical data using SCD Type-2 logic.
* Wrote **custom macros** using Jinja to avoid repetition in models.
* Configured **CI/CD pipeline** (using GitHub Actions) for auto deployment of models on every push.
* Practiced using **DBT tests** (unique, not\_null, relationships) to ensure data quality.

---
Contact

If you’d like to connect or have any questions:

**📧 Email**: [maruthireddynaru@gmail.com](mailto:maruthireddynaru@gmail.com)


This project was a great learning experience and helped me get hands-on with the full lifecycle of DBT — from setup to deployment. Feel free to explore the code, models, and configurations in this repo!


