# task-2-prodigy-infotech
In this task, I performed data cleaning and exploratory data analysis (EDA) on the Diabetes dataset to uncover meaningful patterns and relationships. Handling missing and invalid values and analyzing correlations helped me understand how different health factors influence diabetes outcomes.
#Univariate Analysis Histogram – Age Distribution
plt.figure()
plt.hist(df['Age'], bins=10)
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.title('Age Distribution')
plt.show()

#Bar Chart – Outcome Distribution
df['Outcome'].value_counts().plot(kind='bar')
plt.xlabel('Outcome (0 = Non-Diabetic, 1 = Diabetic)')
plt.ylabel('Count')
plt.title('Diabetes Outcome Distribution')
plt.show()

#Bivariate Analysis (Relationships) Glucose vs Outcome
plt.figure()
plt.boxplot([df[df['Outcome']==0]['Glucose'],
             df[df['Outcome']==1]['Glucose']],
            labels=['Non-Diabetic', 'Diabetic'])
plt.ylabel('Glucose Level')
plt.title('Glucose vs Diabetes Outcome')
plt.show()

#Correlation Analysis
correlation = df.corr()
correlation

plt.figure()
plt.imshow(correlation)
plt.colorbar()
plt.title('Correlation Matrix')
plt.show()







