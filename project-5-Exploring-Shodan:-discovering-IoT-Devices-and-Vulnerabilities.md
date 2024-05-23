# Project 5: Exploring Shodan: Uncovering Internet-Connected Devices and Vulnerabilities

## Introduction

Shodan is a search engine for Internet-connected devices. It allows users to find specific types of devices (e.g., routers, servers, IoT devices) and identify their vulnerabilities. This project will guide you through setting up and using Shodan to uncover information about devices connected to the Internet and their potential security issues.

## Pre-requisites

- Basic understanding of OSINT
- Familiarity with the command line interface
- Shodan account (free or paid) to access the Shodan API
- API key from Shodan

## Lab Set-up and Tools

- **Shodan**: The primary tool for this project
- **Python**: Ensure Python is installed on your system
- **Internet connection**: Required for fetching data from Shodan

### Installation Steps

1. **Install Shodan Python library**:
    ```bash
    pip install shodan
    ```

2. **Obtain your Shodan API key**:
    - Sign up for a Shodan account at [Shodan.io](https://www.shodan.io/)
    - Retrieve your API key from your account dashboard

## Exercises

### Exercise 1: Basic Shodan Search

1. **Initialize Shodan with your API key**:
    ```python
    import shodan

    SHODAN_API_KEY = 'YOUR_API_KEY'
    api = shodan.Shodan(SHODAN_API_KEY)
    ```

2. **Search for devices using a basic query**:
    ```python
    results = api.search('apache')
    for result in results['matches']:
        print(result['ip_str'], result['data'])
    ```
    **Expected Output**: A list of IP addresses and data for devices running Apache servers.

### Exercise 2: Advanced Shodan Search

1. **Use filters to refine your search**:
    ```python
    results = api.search('port:22 country:US')
    for result in results['matches']:
        print(result['ip_str'], result['data'])
    ```
    **Expected Output**: A list of IP addresses and data for devices with SSH (port 22) open in the US.

### Exercise 3: Retrieving Information About a Specific IP

1. **Get detailed information about a specific IP address**:
    ```python
    ipinfo = api.host('8.8.8.8')
    print(ipinfo)
    ```
    **Expected Output**: Detailed information about the device at IP address 8.8.8.8, including open ports, services, and vulnerabilities.

### Exercise 4: Exploring Vulnerabilities

1. **Search for devices with a specific vulnerability (e.g., Heartbleed)**:
    ```python
    results = api.search('vuln:Heartbleed')
    for result in results['matches']:
        print(result['ip_str'], result['vulns'])
    ```
    **Expected Output**: A list of IP addresses for devices vulnerable to Heartbleed, along with vulnerability details.

### Exercise 5: Exporting Results

1. **Save search results to a file for later analysis**:
    ```python
    with open('shodan_results.txt', 'w') as file:
        for result in results['matches']:
            file.write(f"{result['ip_str']} - {result['data']}\n")
    ```
    **Expected Output**: A text file named "shodan_results.txt" containing the search results.

## Conclusion

In this project, you learned how to use Shodan to uncover Internet-connected devices and their vulnerabilities. You installed the Shodan Python library, performed basic and advanced searches, retrieved detailed information about specific IP addresses, explored vulnerabilities, and saved your results for further analysis. Shodan is a powerful tool for OSINT investigations, providing invaluable insights into the security of Internet-connected devices.
