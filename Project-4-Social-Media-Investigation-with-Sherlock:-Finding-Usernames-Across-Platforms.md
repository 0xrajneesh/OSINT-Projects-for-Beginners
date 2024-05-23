# Project 4: Social Media Investigation with Sherlock: Finding Usernames Across Platforms

## Introduction

Sherlock is a powerful tool designed to hunt down social media usernames across various platforms. This project will guide you through installing and using Sherlock to find usernames across multiple social media sites, aiding in OSINT investigations.

## Pre-requisites

- Basic understanding of OSINT
- Familiarity with the command line interface
- A system with Python installed (Sherlock requires Python)

## Lab Set-up and Tools

- **Sherlock**: The primary tool for this project
- **Python**: Ensure Python is installed on your system
- **Internet connection**: Required for fetching data from online sources

### Installation Steps

1. **Install Sherlock**:
    ```bash
    git clone https://github.com/sherlock-project/sherlock.git
    cd sherlock
    pip install -r requirements.txt
    ```

2. **Verify Installation**:
    ```bash
    python3 sherlock --help
    ```
    **Expected Output**: Help menu displaying various options and usage information for Sherlock.

## Exercises

### Exercise 1: Basic Username Search

1. **Run Sherlock to search for a username**:
    ```bash
    python3 sherlock username
    ```
    **Expected Output**: A list of social media platforms and the presence (or absence) of the username "username" on each platform.

### Exercise 2: Search with Multiple Usernames

1. **Run Sherlock to search for multiple usernames**:
    ```bash
    python3 sherlock username1 username2 username3
    ```
    **Expected Output**: Lists of social media platforms showing the presence (or absence) of each specified username.

### Exercise 3: Saving Results to a File

1. **Save the search results to a text file**:
    ```bash
    python3 sherlock username --output results.txt
    ```
    **Expected Output**: Results saved in a file named "results.txt" containing the information about the username across various platforms.

### Exercise 4: Search with Proxy

1. **Run Sherlock with a proxy to hide your IP address**:
    ```bash
    python3 sherlock username --proxy http://127.0.0.1:8080
    ```
    **Expected Output**: The search results for the username using the specified proxy server.

### Exercise 5: Analyzing Results

1. **Open and review the results file**:
    ```bash
    cat results.txt
    ```
    **Expected Output**: Display the contents of "results.txt" showing the usernames' presence across various social media platforms.

## Conclusion

In this project, you learned how to use Sherlock for social media investigations. You installed the tool, performed basic and advanced searches for usernames across multiple platforms, saved the results to a file, and utilized a proxy for anonymity. Sherlock is a valuable tool for uncovering social media presence and can significantly aid in OSINT investigations by providing a quick way to track down usernames.
