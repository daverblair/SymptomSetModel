# SymptomSetModel


## Dependencies

        'numpy',
        'pandas',
        'scipy',
        'PiecewiseBeta',
        'vlpi',
        'scikit-learn',

## Installation

The software package can be installed using pip by running the following command:

pip install SymptomSetModel

##  Basic Instructions

1) Instantiate the model:

    symptom_model=SymptomaticDiseaseModel(list_of_subject_row_ids,list_of_symptom_column_ids,sparse_matrix_of_binary_diagnoses)

2) Build background model for a particular subset of symptoms (recommend using the 'Independent Model', as it the simplest/most validated):

    symptom_model.BuildBackgroundModel(list_of_symptoms,'Independent',TrainingIndex=sample_ids_for_training)

3) Infer penetrance model for a set of carriers:
    
    output=symptom_model.FitPenetranceModel(list_of_carriers)
    



