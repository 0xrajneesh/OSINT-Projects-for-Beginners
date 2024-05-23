# Project 1: Hands-on with Recon-ng: A Comprehensive Reconnaissance Framework

## Introduction

Recon-ng is a full-featured reconnaissance framework designed for open-source intelligence (OSINT) gathering. It provides a powerful and flexible environment for collecting data from various sources using a modular approach. This project will introduce you to the basics of Recon-ng, including installation, setup, and using modules to gather information about a target domain.

## Pre-requisites

- Basic understanding of OSINT
- Familiarity with the command line interface
- A system with Python installed (Recon-ng requires Python)

## Lab Set-up and Tools

- **Recon-ng**: The primary tool for this project
- **Python**: Ensure Python is installed on your system
- **Internet connection**: Required for fetching data from online sources

### Installation Steps

1. **Install Recon-ng**:
    ```bash
    git clone https://github.com/lanmaster53/recon-ng.git
    cd recon-ng
    pip install -r REQUIREMENTS
    ```

2. **Launch Recon-ng**:
    ```bash
    ./recon-ng
    ```

## Exercises

### Exercise 1: Basic Navigation and Setup

1. **Start Recon-ng**:
    ```bash
    ./recon-ng
    ```
    **Expected Output**: You should see the Recon-ng prompt.

2. **View available modules**:
    ```shell
    > show modules
    ```
    **Expected Output**: A list of available modules categorized by their purpose (e.g., discovery, exploitation, reporting).

3. **Set a workspace**:
    ```shell
    > workspaces add my_first_workspace
    ```
    **Expected Output**: Confirmation that the workspace "my_first_workspace" has been created and switched to.

### Exercise 2: Gathering Domain Information

1. **Set the target domain**:
    ```shell
    > set domain example.com
    ```
    **Expected Output**: Confirmation that the domain has been set to "example.com".

2. **Load and run a domain information module**:
    ```shell
    > use recon/domains-hosts/bing_domain_web
    > run
    ```
    **Expected Output**: Output showing the hosts discovered related to "example.com".

### Exercise 3: Collecting WHOIS Data

1. **Load the WHOIS module**:
    ```shell
    > use recon/domains-hosts/whois_pocs
    ```
    **Expected Output**: The module should be loaded.

2. **Run the WHOIS module**:
    ```shell
    > run
    ```
    **Expected Output**: WHOIS information about the target domain, including registrant details.

### Exercise 4: Extracting Email Addresses

1. **Load the email harvesting module**:
    ```shell
    > use recon/domains-contacts/pgp_search
    ```
    **Expected Output**: The PGP search module should be loaded.

2. **Run the module to find email addresses**:
    ```shell
    > run
    ```
    **Expected Output**: A list of email addresses associated with the target domain.

### Exercise 5: Reporting

1. **Generate a report of collected data**:
    ```shell
    > use reporting/csv
    > set filename my_report.csv
    > run
    ```
    **Expected Output**: A CSV file named "my_report.csv" containing all the collected data.

## Conclusion

In this project, you learned how to use Recon-ng for OSINT gathering. You navigated through its interface, set up a workspace, and used various modules to gather domain information, WHOIS data, and email addresses. Finally, you generated a report of the collected data. Recon-ng is a versatile tool, and with further exploration, you can uncover a wealth of information using its extensive module library.
