# Project 2: Harvesting Data with theHarvester: Email, Subdomain, and Host Information Gathering

## Introduction

theHarvester is a powerful tool used for gathering email addresses, subdomains, and hostnames from various public sources such as search engines and PGP key servers. This project will guide you through installing and using theHarvester to collect valuable information about a target domain.

## Pre-requisites

- Basic understanding of OSINT
- Familiarity with the command line interface
- A system with Python installed (theHarvester requires Python)

## Lab Set-up and Tools

- **theHarvester**: The primary tool for this project
- **Python**: Ensure Python is installed on your system
- **Internet connection**: Required for fetching data from online sources

### Installation Steps

1. **Install theHarvester**:
    ```bash
    git clone https://github.com/laramies/theHarvester.git
    cd theHarvester
    pip install -r requirements.txt
    ```

2. **Verify Installation**:
    ```bash
    python3 theHarvester.py -h
    ```
    **Expected Output**: Help menu displaying various options and usage information for theHarvester.

## Exercises

### Exercise 1: Basic Usage

1. **Run theHarvester to gather emails and subdomains from a target domain**:
    ```bash
    python3 theHarvester.py -d example.com -b google
    ```
    **Expected Output**: A list of email addresses and subdomains related to "example.com" obtained from Google.

### Exercise 2: Collecting Data from Multiple Sources

1. **Run theHarvester using multiple data sources**:
    ```bash
    python3 theHarvester.py -d example.com -b google,bing,linkedin
    ```
    **Expected Output**: Aggregated list of email addresses, subdomains, and hostnames from Google, Bing, and LinkedIn.

### Exercise 3: Saving Results to a File

1. **Save the results to a file for later analysis**:
    ```bash
    python3 theHarvester.py -d example.com -b google -f results.txt
    ```
    **Expected Output**: Results saved in a file named "results.txt" containing the harvest
