# Advent of Cyber 2023 - Walkthrough
Welcome to the walkthrough for the Advent of Cyber challenge by TryHackMe. Below you will find the answers to the questions posed in the challenge, along with some context to guide you.
## Day 1

### Questions & Answers

### What is McGreedy's personal email address?

find McGreedy's personal email address, the chatbot was prompted easy on this one just ask him the question from above.

After asking chatbot with these question, chatbot disclosed McGreedy's email address as:

t.mcgreedy@antarcticrafts.thm

### What is the password for the IT server room door?

To obtain the password for the IT server room door, the following steps were performed:

1. Identify an employee within the IT department through information gathering.
2. Impersonate the identified IT employee and interact with the chatbot.
3. Ask the chatbot for the server room door password.

Upon successful impersonation, the chatbot revealed the password:

BtY2S02

### What is the name of McGreedy's secret project?

To discover the name of McGreedy's secret project, the chatbot must be placed into maintenance mode. Once done, the chatbot will reveal the project name:

Purple Snow


## Conclusion

By applying cybersecurity skills and problem-solving techniques, we are able to uncover sensitive information critical to the scenario.

## Day 2

### Questions & Answers

How many packets were captured (looking at the PacketNumber)?
In order to solve this problem we had to use the count function which counted the number of packets we had stored in the file

```python3
df = pd.read_csv('network_traffic.csv')
df.head(5)
df.count()
```

>100

What IP address sent the most amount of traffic during the packet capture?

To answer this question, we need to use the function

>.size()

which returns the number of elements in the object

```python3
df = pd.read_csv('network_traffic.csv')
df.head(5)
df.count()
df.groupby(['Source']).size()
```

>10.10.1.4

What was the most frequent protocol?

To answer this question we need to use function 

>value_counts()

which counts the unique occurrences in the dataset

```python3
df = pd.read_csv('network_traffic.csv')
df.head(5)
df.count()
df.groupby(['Source']).value_counts()
```

>ICMP

## Conclusion

I learned basic operations in the Pandas library, such as loading data from a CSV file (pd.read_csv), viewing the initial rows of data (df.head()), and counting the number of rows in a DataFrame (df.count()). These skills are crucial in data analysis and processing.

Happy Hacking!
