# Poem_Segmentation

Preprocessing function is designed to perform tokenization on the poem. It transforms the poem text in to a list of lines 
The function uses poem.split('\n') to split the entire poem into individual lines based on the newline character (\n). This results in a list of lines.
line.strip() is applied to each line. it helps in removing any white spaces 
The condition if line.strip() ensures that only non-empty lines are included in the final list. If line.strip() evaluates to an empty string (meaning the line was either empty or contained only whitespace), it will be excluded from the result.

Create embeddings based on the sentences generated after preprocessing.
Using the pre-trained emotion model “j-hartmann/emotion-english-distilroberta-base” , detect emotions in the sentences and then extract the emotion with the highest score.
Calculate cosine similarity between the embeddings.

SEGMENTATION:If the cosine similarity between two embeddings is greater than the set threshold and there is an emotion change at the same time, a new segment is generated.
