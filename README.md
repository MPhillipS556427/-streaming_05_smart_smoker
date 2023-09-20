# streaming 05: Smart BBQ Smoker Temperature
Publisher: Malcolm Phillip
Date:  19 September 2023

## Overview
This project is a Python script designed to read temperature data from a CSV file and send it to RabbitMQ queues for monitoring. Additionally, it opens the RabbitMQ Admin website for real-time monitoring of the queues. The script is intended for use in scenarios like monitoring a BBQ smoker and the temperatures of multiple foods being cooked in it. In this project youll find two files to practice with, the logger producer file and the normal producer file.

## Prerequisites
1. Git
1. Python 3.7+ (3.11+ preferred)
1. VS Code Editor
1. VS Code Extension: Python (by Microsoft)
1. RabbitMQ Server installed and running locally
1. pika 1.3.2 (or recent)
1. Logger 
1. Webbrowser
1. sys
1. Time
1. csv

## How to Run the Code
1. Prepare Your CSV File: Ensure that you have a CSV file containing temperature data. The CSV file should have columns for the timestamp and temperature readings for a smoker and two foods, as specified in the script. The default CSV file name is smoker-temps.csv, but you can change it in the script by modifying the csv_file_name variable.

1. Run the Script: Open a terminal or command prompt and navigate to the directory where the script is located. Then, run the script using the following command: python smoker_bbq_producer.py 
### Terminal Screenshot:
![Alt text](<Screenshot 2023-09-20 at 7.11.13 AM.png>)


1. Monitoring RabbitMQ Admin Website: The script will open the RabbitMQ Admin website in your default web browser. You can monitor the RabbitMQ queues from there. If you don't want the website to open automatically, set show_offer to False in the script.

### RabbitMQ Admin Website Screenshot:
![Alt text](<Screenshot 2023-09-20 at 7.11.41 AM.png>)

1. Script Execution: The script will read data from the CSV file, parse it, and send temperature readings to RabbitMQ queues. It will repeat this process with a sleep interval of 30 seconds between readings. If any errors occur during execution, they will be logged to a file named Smart_BBQ_Smoker.log in the same directory as the script.

1. Exiting the Script: You can safely exit the script by pressing Ctrl+C in the terminal or command prompt. The script will log the exit message.

1. ogging: You can check the log file (Smart_BBQ_Smoker.log) for detailed information about the script's execution, including any errors encountered.

## Note: Please make sure you have configured the CSV file with valid data and RabbitMQ server settings before running the script.

## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)

- See https://github.com/MPhillipS556427/streaming-03-rabbitmq.git and https://github.com/MPhillipS556427/streaming-04-multiple-consumers.git for remedial training exercises to assist prior to executing this project.
