# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
# EXNO-5-DS : Data Visualization using Matplotlib Library

# STEP 1: Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt

# STEP 2: Create sample data
data = {
    'Student': ['John', 'Alice', 'Bob', 'Diana', 'Eva'],
    'Maths': [88, 92, 79, 93, 85],
    'Science': [90, 85, 76, 89, 95],
    'English': [78, 82, 74, 88, 90]
}

# Convert dictionary to DataFrame
df = pd.DataFrame(data)
print("Input Data:\n", df)

# STEP 3: LINE CHART – Compare subject scores for each student
plt.figure(figsize=(8,5))
plt.plot(df['Student'], df['Maths'], marker='o', label='Maths')
plt.plot(df['Student'], df['Science'], marker='s', label='Science')
plt.plot(df['Student'], df['English'], marker='^', label='English')
plt.title("Student Performance Comparison")
plt.xlabel("Student Name")
plt.ylabel("Marks Scored")
plt.legend()
plt.grid(True)
plt.show()

# STEP 4: BAR CHART – Visualize Maths scores
plt.figure(figsize=(7,5))
plt.bar(df['Student'], df['Maths'], color='teal')
plt.title("Maths Marks of Students")
plt.xlabel("Student")
plt.ylabel("Marks")
plt.show()

# STEP 5: HISTOGRAM – Distribution of Science marks
plt.figure(figsize=(7,5))
plt.hist(df['Science'], bins=5, color='orange', edgecolor='black')
plt.title("Distribution of Science Marks")
plt.xlabel("Marks Range")
plt.ylabel("Number of Students")
plt.show()

# STEP 6: SCATTER PLOT – Relation between Maths and Science
plt.figure(figsize=(6,5))
plt.scatter(df['Maths'], df['Science'], color='purple', s=100)
plt.title("Maths vs Science Performance")
plt.xlabel("Maths Marks")
plt.ylabel("Science Marks")
plt.show()

# STEP 7: PIE CHART – Percentage of total marks of each student
df['Total'] = df[['Maths','Science','English']].sum(axis=1)
plt.figure(figsize=(6,6))
plt.pie(df['Total'], labels=df['Student'], autopct='%1.1f%%', startangle=90, colors=['#ff9999','#66b3ff','#99ff99','#ffcc99','#c2c2f0'])
plt.title("Percentage of Total Marks by Each Student")
plt.show()



<img width="342" height="219" alt="Screenshot 2025-10-16 105742" src="https://github.com/user-attachments/assets/7f6d4af7-1d8a-46f7-9e30-b69169dd0012" />

# Result:
    The above code executed sucessfully
