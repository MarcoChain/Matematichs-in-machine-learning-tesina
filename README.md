# Introduction 
  
The focus of this project consist of some algorithms and techniques explained during the Mathematics and Machine Learning course. In particular, regards to supervised learning part, the following topics will be covered:

-   K-Nearest Neighbor (KNN)
-   Decision tree
-   Random forest
-   Linear support-vector machines (Linear SVM)
-   Logistic regression

As regards the unsupervised part, the concentration will relate to:

-   Principal Component Analysis (PCA)
-   K-means clustering

All these algorithms will be explained in detail during the preparation of this report, and in relation to most of them, our implementation from scratch will also be provided using the Numpy library. Having said that, we will not focus on how to choose good parameters or how to get a good score: we will therefore omit the cross validation part and the data set will be divided only by train and test set. To better understand the reasons behind this decision, it is necessary to carefully consider the dataset chosen.

# The dataset and the problem
It is therefore a small dataset - less than three hundred observations. As already mentioned, given the small number, it is difficult to divide it into more than two parts, therefore the validation set will be omitted. Moreover, when dealing with small data sets, it is often difficult to get a good result, so we will not perform any kind of hyperparameter tuning. Anyway, before we start applying any kind of algorithm or plotting something, let's take a look at what we're talking about from a medical point of view.

Heart attack is due to a thrombosis of a coronary artery of the heart, or in any case to an occlusion of it. The most frequent cause of closure of an artery is arteriosclerosis: the presence of plaques of solid material that accumulates in the artery until it creates a plug. In this case we speak about thrombosis. If the blood does not arrive because of this closure, oxygen and nourishment will be lacking and the tissue cells will die and the damage becomes irreversible.

Risk factors Heart attack mainly affects adults and elderly subjects with cardiovascular risk factors, including arterial hypertension, diabetes mellitus, hypercholesterolemia, obesity, cigarette smoking, familiarity for ischemic heart disease. Epidemiology and statistics have made possible to identify numerous risk factors - both personal and environmental - that can predispose to coronary artery diseases such as atherosclerosis, angina pectoris, heart attack. These are the so-called "coronary risk factors". One or more of these conditions are found in individuals with heart attack almost without exception. The risk factors are therefore divided into two categories:
1) Uncorrectable:

-   Gender: men are more affected than women.
-   Heredity: those who have family members affected by coronary heart disease are more likely to get sick than those who are not familiar with it.
-   Diabetes (fasting blood sugar > 120 mg/dL): causes alterations of the small arteries that facilitate the onset of cardiovascular diseases.
-   Age: as we age, the chances of heart disease increase.

2) Correctable:

-   Smoking: smokers are more exposed to heart, arterial and lung diseases than non-smokers.
-   Hypercholesterolemia: it promotes the formation of fat deposits and atherosclerotic plaques on the walls of the arteries which restrict the lumen by hindering the flow of blood.
-   High blood pressure: forces the heart to overwork and favors lesions of the arteries. Hypertensive subjects have a higher incidence of diseases of the heart, vessels, kidneys compared to people with normal blood pressure.

The "coronary risk factors" are divided, according to their importance, into major and minor: smoking, hypertension, excess blood cholesterol, diabetes and lack of physical activity are among the first. The simultaneous presence of multiple risk factors in the same individual increases the probability of being affected by coronary heart disease with geometric progression. For example, the risk of heart attack for an average smoker is double compared to a non-smoker: if he also has too much cholesterol in the blood and high blood pressure the risk becomes sixteen times greater.
CPS

The Chest Pain Score (CPS) - introduced by Geleijnse in 2000 - consists of a scoring that evaluates the probability that a subject may have a myocardial infarction given the symptoms clinically presented. This index is an independent risk factor for acute heart attack, and evaluates 4 parameters: pain characteristics, pain localization, pain irradiation, pain associated symptoms. The overall CPS score can be between -2 and +9: a value <4 defines an “atypical chest pain”, of non-cardiac origin, if the score is ≥4, we speak about “typical chest pain”, which is an indication of probable myocardial ischemia. The CPS showed a sensitivity of 87.5% and a specificity of 62.5%.

Diagnosis

The diagnosis of heart attack takes advantage of the contribution of the electrocardiogram (ECG) and of blood tests capable of detecting the presence of "markers" of myocardial cell necrosis in the blood (troponin, myoglobin, MB isoenzyme of the CK, ALT, AST , LDH). If the ECG trace shows non-specific and not clearly diagnostic anomalies, it is possible to deepen the study of the coronary arteries by subjecting the patient to a cycle-ergometric test (stress test). This consists in letting the patient pedal on a cyclette. The intensity of effort and the force required to perform it (workload) are gradually increased. The ECG is monitored continuously and blood pressure is measured at regular time intervals. The subject is usually asked to continue until he reaches a heart rate between 80 and 90% of the maximum heart rate, by age and gender. If and when symptoms, such as wheezing or chest pain, become too annoying, or if and when significant ECG abnormalities appear, the examination is stopped. The parameters that are assessed on the reading of the stress test are represented by: appearance of the ECG at rest, maximum heart rate reached at the peak of the effort, the appearance of symptoms, alterations of the ST segment during the effort (ST depression), and the slope of the peak ofST segment during exercise.

Therapeutic approach

Until the 1990s, the study of the coronary arteries was carried out by fluoroscopy. Fluoroscopy is a radiological technique that was used to obtain real-time images of the internal anatomy of a patient's coronary arteries through the use of a fluoroscope. In its simplest form, a fluoroscope was composed of an X-ray source and a fluorescent screen coupled to an image intensifier that allowed the obtained images to be recorded and reproduced on paper or monitor, between which the patient was positioned.
# The development

To look at the details and all the algorithms implemented looks at my tesina [heart_study.ipynb](https://github.com/MarcoChain/Matematichs-in-machine-learning-tesina/blob/master/heart_study.ipynb).
> Written by[MarcoChain](https://www.linkedin.com/in/marcogullotto/).
