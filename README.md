# Converting CoLab Notebooks to JupyterLab Notebooks (Windows)

Welcome! This repository is dedicated to converting CoLab notebooks to JupyterLab notebooks, specially designed for Windows systems. 

## Introduction
Google Colaboratory (CoLab) is a great tool for data science and machine learning practitioners who want to work in a notebook environment. However, there are several reasons one might want to convert CoLab notebooks to JupyterLab notebooks:

1. **Offline Access:** JupyterLab notebooks can be accessed and worked on offline, which is not possible with CoLab notebooks.
2. **Customization:** JupyterLab offers more customization options compared to CoLab.
3. **Server Control:** With JupyterLab, you have control over the server, which is not the case with CoLab.

## Status
This is a "work in progress" repository, and I am still learning. Any contributions, suggestions, or feedback are highly appreciated.


Dataset Tagger:

# Dataset AutoTagger Notebook Setup Guide

The first notebook in this repository is a Dataset AutoTagger. Follow this guide to set it up:

## Prerequisite
Make sure you have installed "chocolatey". Execute the following command as Admin in Powershell:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

## Setup Instructions

### Cellblock 1:
1. Line 5 - Set your Root Folder (Working folder Structure: Lora/project_name/dataset)
2. Line 8 - Enter your Project Name
3. Hit Run

### Cellblock 2:
1. Line 8 - Check the Blacklisted Tags. Make sure they are suited for your Dataset.
2. Hit Run

### Cellblock 3:
1. Line 9 - Put an activation tag at the start of every text file. This is useful to make learning better and activate your Lora easier.
2. Line 10 - Common tags that are removed such as hair color, etc. will be "absorbed" by your activation tag.

## Advanced Settings

For advanced users, there are more settings available:

```
search_tags = "" #@param {type:"string"}
replace_with = "" #@param {type:"string"}
search_mode = "OR" #@param ["OR", "AND"]
new_becomes_activation_tag = False #@param {type:"boolean"}
sort_alphabetically = False #@param {type:"boolean"}
remove_duplicates = False #@param {type:"boolean"}
```

Adjust these parameters as needed for your specific use case.

