# Sorting Hat - Discussion

## Which questions to remove:
Based on feature ranking analysis from the trained decision tree model, not all 10 questions contributed equally to house prediction. Specifically, questions 4, 5, 7, and 8 had an importance score of 0.000, meaning the model never used them in any split.

Rank    Question No.    Feature Importance  
1       Q9              0.260  
2       Q6              0.204  
3       Q10             0.197  
4       Q1              0.119  
5       Q3              0.112  
6       Q2              0.109  
7–10    Q4, Q5, Q7, Q8  0.000  

To improve user experience and reduce quiz length, I would remove Q4, Q5, Q7, Q8.

## Improving accuracy and efficiency:
•	Data collection: Increasing dataset size and ensuring balanced house labels.  
•	Tree pruning: Limiting depth or applying post-pruning improves generalization and memory footprint on the ESP32.

## Additional sensors and hardware: 
•	RGB LED for house color feedback  
•	Piezo buzzer or speaker for audio output (e.g. “You belong in Ravenclaw!”)  
These enhancements would make the system more immersive, especially for younger users.

## Is a decision tree still suitable?
Yes, a decision tree remains suitable with the addition of RGB LEDs and a piezo buzzer or speaker. These components are output-only hardware and do not introduce new types of input data into the model. Since the model's input structure and feature format remain unchanged (still based on button responses), the existing decision tree can be used without modification. The added hardware simply enhances the user experience by providing visual and audio feedback.


![12a4f2bcb88dac1753c8662a7a4d2d2](https://github.com/user-attachments/assets/9d6fbafa-47b3-44e1-8163-9a0591844bc3)
