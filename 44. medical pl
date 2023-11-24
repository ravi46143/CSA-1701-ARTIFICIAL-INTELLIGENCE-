% Define symptoms and diseases
symptom(john, fever).
symptom(john, cough).
symptom(john, headache).

symptom(susan, fever).
symptom(susan, sore_throat).
symptom(susan, fatigue).

disease(cold, [fever, cough, headache]).
disease(flu, [fever, cough, fatigue]).
disease(strep_throat, [fever, sore_throat, fatigue]).

% Define rules for diagnosis
diagnose(Patient, Disease) :-
    symptom(Patient, Symptom),
    disease(Disease, Symptoms),
    check_symptoms(Symptom, Symptoms).

check_symptoms(_, []).
check_symptoms(Symptom, [Symptom | _]).
check_symptoms(Symptom, [_ | Rest]) :-
    check_symptoms(Symptom, Rest).
