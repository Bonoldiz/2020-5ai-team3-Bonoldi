# **System Documentation**

**Team 3** - February 27, 2020

**Team Members:** Ambrosi Marco, Bonoldi Enrico, Lorenzoni Luca

# Contents

Contents 

**1. Introduction** 

**2. Setup Laravel and React**

**3. Connect the project to SIGMA database**

**4. System Maintenance**
<br>
**Revision History**

| **Version** | **Date** | **Name** | **Description** |
| --- | --- | --- | --- |
| 1 | 27/02/20 | Marco Ambrosi | Initial Document |

# 1. Introduction

The PCTO Manager application allows users to access every student&#39;s internship experiences. This document will provide instructions for accessing the application code and installing it into a machine that will function as a server.

# 2. Setup Laravel and React

Everything you need to install the application (which means Laravel / React) is saved as a Docker image in an online repository:

[https://github.com/Bonoldiz/PCTO](https://github.com/Bonoldiz/PCTO)

The repository is private, so you have to ask the owner in order to access it.

Once you&#39;ve done that, you&#39;re ready to launch the appropriate &quot;clone&quot; Git command to clone the repository, then you must create a Docker container from the downloaded image and run the container itself. More information on required Git and Docker commands here:

[https://docs.docker.com/get-started/part2/](https://docs.docker.com/get-started/part2/)

# 3. Connect the project to SIGMA database

In order to connect to the school&#39;s SIGMA database, you&#39;ll need to modify the &quot;DATABASE&quot; entry and the relative ip, username and password inside Laravel&#39;s &quot;.env&quot; file. This will ensure that the right parameters are set to establish a successful connection to SIGMA.

# 4. System Maintenance

PCTO Manager uses its own Web API to obtain information, that will be returned as a combination of Spaggiari&#39;s SOAP API Service&#39;s data and SIGMA&#39;s database data. This is possible thanks to the project&#39;s ETL and Web API: the first will format Spaggiari&#39;s data in order to be compatible with SIGMA&#39;s data, while the second will submit the users&#39; queries to SIGMA. From a user&#39;s point of view, an easily readable report on what was asked will be displayed on screen, where the user will be able to modify various internship experiences as well as utilize the website in its integrity.
