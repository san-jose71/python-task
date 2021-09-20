import pandas as pd
import re

data = pd.read_csv("users.csv")
correct_df = data.copy()
correct_df.rename(columns={'name': 'name', 'surname': 'surname', 'email\t': 'email'}, inplace=True)
#Exporting to CSV file
correct_df.to_csv(r'users.csv', index=False,header=True)
