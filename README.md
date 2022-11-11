# SpaCy: Extracting Custom Multi-Word Entities for building an NER model

This notebook depicts the first segment in the code for building a custom Named Entity Recognition model with SpaCy. 

The initial csv had a column of string data indicating job descriptions. SpaCy's default entity recognizer extracted all numbers and labelled them as 'CARDINAL' - this included addresses, contact numbers, quantities and more. After analysing the data, regex rules were created in order to extract meaningful entities and labels. Since the entities needed were phrases and not single words, SpaCy's 'Span' and 'Filter Span' packages were used to extract them. Span is used to extract multiple words from the text; filter span prioritizes longer entities in order to prevent overlap between them. The trim entity spans function removed trailing and ending spaces from the entities. 

## Evaluation

The entities from the real and predicted test sets were converted to vector matrices. Each non-entity was tokenized as 'O'. Using the two matrices, a confusion matrix was visualized and a classification report generated.  

