As a part of my Google Advanced Data Analytics courses, I must analyse this data set. Here is the explanation:
Salifort Motors is a fictional French-based alternative energy vehicle manufacturer. Its global workforce of over 100,000 employees research, design, construct, validate, and distribute electric, solar, algae, and hydrogen-based vehicles. Salifort’s end-to-end vertical integration model has made it a global leader at the intersection of alternative energy and automobiles.

- We have received the results of a recent employee survey. We were asked with analyzing the data to come up with ideas for how to increase employee retention. To help with this, they would like us to design a model that predicts whether an employee will leave the company based on their  department, number of projects, average monthly hours, and any other data points we deem helpful. A good model will help the company increase retention and job satisfaction for current employees, and save money and time training new employees. 
- We did Exploratory data analysis and it turned out that :
     - Employees who left fall into two general categories: dissatisfied employees with shorter tenures and very satisfied employees with medium-length tenures.
     - Four-year employees who left seem to have an unusually low satisfaction level.
     - The longest-tenured employees didn't leave. Their satisfaction levels aligned with those of newer employees who stayed.

- It appears that employees are leaving the company as a result of poor management. Leaving is tied to longer working hours, many projects, and generally lower satisfaction levels. It can be ungratifying to work long hours and not receive promotions or good evaluation scores. There's a sizeable group of employees at this company who are probably burned out. It also appears that if an employee has spent more than six years at the company, they tend not to leave.
- Then, we built three models, logistic regression, decision tree and random forest.
- The logistic regression model achieved precision of 80%, recall of 83%, f1-score of 80% (all weighted averages), and accuracy of 83%, on the test set.
- For tree based modeling, we did build each of them twice. Once with all the features and second, with just some of them. Because there was a chance that there was some data leakage occurring. It was likely that the company wouldn't have satisfaction levels reported for all of its employees. It's also possible that the average_monthly_hours column was a source of some data leakage. If employees have already decided upon quitting, or have already been identified by management as people to be fired, they might be working fewer hours.
- So, for the next round of tree based models we would incorporate feature engineering to build improved models.
- We dropped satisfaction_level and created a new feature that roughly captures whether an employee is overworked. We called this new feature overworked. It would be a binary variable.
- The decision tree model achieved AUC of 93.8%, precision of 87.0%, recall of 90.4%, f1-score of 88.7%, and accuracy of 96.2%, on the test set. The random forest modestly outperformed the decision tree model.
  
![decision-capstone](https://github.com/user-attachments/assets/c8df1041-cd54-4a3c-a629-49144d5c3d4a)

![downloadc7](https://github.com/user-attachments/assets/f3d14bfd-cefd-4d60-bbfd-83c49a276a85)


I hope you liked this project!
