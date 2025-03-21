This is the repositiory of my graduation project tittled  : "Implementing a constraint acquisition system called Quacq using python and enhancing it with natural language processing (NLP)"

Data:
It contains the different data files generated for classification and named entity recognition in a csv format. For the NER data, we a folder
for each constraint type we worked on, and 4 versions of the annotated data. The version we used for the latest models is the fourth 
version in each of four constraint types. Then, we have a folder called scripts, it contains scripts used to prepare the data and to show
some statistics about each file. Also, we have a script to transform the format generated by the annotation software Doccano to the format
required by the open source BERT implementation we used.

Models:
This folder contains the classification and NER models we used. However, if this directory is downloaded online, they wont be present because
their sizes are big. However, you can refer to the links provided in Models/Models/ModelsDriveLinks.txt to download them separately from 
google drive. Also, we have the evaluation results of these models stored inside this folder alongside a script to read their content. We 
have also the finetuning scripts for both the classification and NER.


QuAcq:
This is the original algorithm's implementation. The one using the exact solver can be found in the exact folder and the same for the ortools solver. We have also the files containing the results of the experimentation; the metrics of each one from the ten runs for each problem. And we have a script to read these results. Some older results are also present but they can be simply ignored.

QuAcqBERT:
This is the nlp version of quacq. we put here the scripts and also the results of the experiments and also the files used to do the experiments using random expressions generated by ChatGPT.

They are arranged like this:

56 directories, 305 files. 

```
.
├── Data
│   ├── Classification
│   │   └── classif23classes.csv
│   ├── NamedEntityRecognition
│   │   ├── binaryConstraints
│   │   │   ├── firstAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── binaryData.csv
│   │   │   │   └── generatedData.txt
│   │   │   ├── fourthAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── binaryData.csv
│   │   │   │   ├── binaryData_justParams.csv
│   │   │   │   └── generatedData.txt
│   │   │   ├── secondAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── binaryData.csv
│   │   │   │   └── generatedData.txt
│   │   │   └── thirdAttempt
│   │   │       ├── admin.jsonl
│   │   │       ├── binaryData.csv
│   │   │       ├── binary_justParams.csv
│   │   │       └── generatedData.txt
│   │   ├── distances
│   │   │   ├── firstAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── adminUnary.jsonl
│   │   │   │   ├── distances.csv
│   │   │   │   ├── distancesUnary.csv
│   │   │   │   ├── generatedData.txt
│   │   │   │   └── generatedDataUnary.txt
│   │   │   ├── fourthAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── adminUnary.jsonl
│   │   │   │   ├── distancesBinary.csv
│   │   │   │   ├── distancesBinary_justParams.csv
│   │   │   │   ├── distancesUnary.csv
│   │   │   │   ├── distancesUnary_justParams.csv
│   │   │   │   ├── generatedData.txt
│   │   │   │   └── generatedDataUnary.txt
│   │   │   ├── secondAttempt
│   │   │   │   ├── admin.jsonl
│   │   │   │   ├── adminUnary.jsonl
│   │   │   │   ├── distances.csv
│   │   │   │   ├── distancesUnary.csv
│   │   │   │   ├── generatedData.txt
│   │   │   │   └── generatedDataUnary.txt
│   │   │   └── thirdAttempt
│   │   │       ├── admin.jsonl
│   │   │       ├── adminUnary.jsonl
│   │   │       ├── distances.csv
│   │   │       ├── distances_justParams.csv
│   │   │       ├── distancesUnary.csv
│   │   │       ├── distancesUnary_justParams.csv
│   │   │       ├── generatedData.txt
│   │   │       └── generatedDataUnary.txt
│   │   └── UnaryConstraints
│   │       ├── Attempt1
│   │       │   ├── admin.jsonl
│   │       │   ├── generatedData.txt
│   │       │   └── UnaryConstraints.csv
│   │       ├── Attempt2
│   │       │   ├── admin.jsonl
│   │       │   ├── generatedData.txt
│   │       │   └── UnaryConstraints.csv
│   │       ├── Attempt3
│   │       │   ├── admin.jsonl
│   │       │   ├── generatedData.txt
│   │       │   ├── UnaryConstraints.csv
│   │       │   └── UnaryConstraints_justParams.csv
│   │       └── Attempt4
│   │           ├── admin.jsonl
│   │           ├── generatedData.txt
│   │           ├── unaryData.csv
│   │           └── unaryData_justParams.csv
│   └── Scripts
│       ├── FromDOCCANO_TO_MODELS.ipynb
│       ├── prepareDataForClassif28classes.ipynb
│       ├── prepareDataForNERNoConstraintType.ipynb
│       └── read_DataStats.ipynb
|
├── Models
│   ├── EvaluationResults
│   │   ├── Files
│   │   │   ├── resultsBinaryData.txt
│   │   │   ├── resultsDistances.txt
│   │   │   ├── resultsDistancesUnary.txt
│   │   │   ├── resultsperTagBinaryDatatxt
│   │   │   ├── resultsperTagDistances.txt
│   │   │   ├── resultsperTagDistancesUnary.txt
│   │   │   ├── resultsperTagUnaryConstraints.txt
│   │   │   └── resultsUnaryConstraints.txt
│   │   └── read_modelsStats.ipynb
│   ├── FineTunningScripts
│   │   ├── Classification
│   │   │   └── finetune_bert_classif_23Classes.ipynb
│   │   └── NER
│   │       └── nerbertval-tofocusonnow-justparams-fourthattemp.ipynb
│   └── Models
│       ├── ModelsDriveLinks.txt
│       ├── ner-bert-alldiffner0.ckpt
│       ├── ner-bert-binaryData.ckpt
│       ├── ner-bert-distances.ckpt
│       ├── ner-bert-distancesUnary.ckpt
│       └── ner-bert-unaryConstraints.ckpt
├── QuAcq
│   ├── Scripts
│   │   └── read_results.ipynb
│   └── V7_Latest_AllMetrics
│       ├── exact
│       │   ├── QuAcq_V7_golomb_latest_allmetrics_exact.ipynb
│       │   ├── QuAcq_V7_JigSaw_latest_allmetrics_exact.ipynb
│       │   ├── QuAcq_V7_purdey_latest_allmetrics_exact.ipynb
│       │   ├── QuAcq_V7_random_latest_allmetrics_exact.ipynb
│       │   ├── QuAcq_V7_Suduku_latest_allmetrics_exact.ipynb
│       │   ├── QuAcq_V7_Zebra_latest_allmetrics_exact.ipynb
│       │   └── resFiles
│       │       ├── resgolomb10runsP1.txt
│       │       ├── resgolomb10runsP2.txt
│       │       ├── resjigsaw10runsP1.txt
│       │       ├── resjigsaw10runsP2.txt
│       │       ├── resjigsaw10runsP3.txt
│       │       ├── respurdey10runs.txt
│       │       ├── resrandom10runs.txt
│       │       ├── ressuduku10runsP1.txt
│       │       ├── ressuduku10runsP2.txt
│       │       ├── ressuduku10runsP3.txt
│       │       └── reszebra10runs.txt
│       └── ortools
│           ├── 10runsResults
│           │   ├── old
│           │   │   ├── resgolomb10runs.txt
│           │   │   ├── resjigsaw10runsP1.txt
│           │   │   ├── resjigsaw10runsP2.txt
│           │   │   ├── resjigsaw10runsP3.txt
│           │   │   ├── respurdey10runs.txt
│           │   │   ├── resrandom10runs.txt
│           │   │   ├── ressuduku10runsP1.txt
│           │   │   ├── ressuduku10runsP2.txt
│           │   │   ├── ressuduku10runsP3.txt
│           │   │   └── reszebra10runs.txt
│           │   ├── older
│           │   │   ├── QuAcq_V7_golomb_latest_allmetrics.ipynb
│           │   │   ├── QuAcq_V7_JigSaw_latest_allmetrics.ipynb
│           │   │   ├── QuAcq_V7_random_latest_allmetrics.ipynb
│           │   │   ├── QuAcq_V7_Suduku_latest_allmetrics.ipynb
│           │   │   ├── QuAcq_V7_Zebra_latest_allmetrics.ipynb
│           │   │   ├── resgolomb10runs_old.txt
│           │   │   ├── resjigsaw10runsP1_old.txt
│           │   │   ├── resjigsaw10runsP2_old.txt
│           │   │   ├── resjigsaw10runsP3_old.txt
│           │   │   ├── respurdey10runs_old.txt
│           │   │   ├── resrandom10runs_old.txt
│           │   │   ├── ressuduku10runsP1_old.txt
│           │   │   ├── ressuduku10runsP2_old.txt
│           │   │   ├── ressuduku10runsP3_old.txt
│           │   │   └── reszebra10runs_old.txt
│           │   ├── resgolomb10runs.txt
│           │   ├── resjigsaw10runsP1.txt
│           │   ├── resjigsaw10runsP2.txt
│           │   ├── resjigsaw10runsP3.txt
│           │   ├── respurdey10runs.txt
│           │   ├── resrandom10runs.txt
│           │   ├── ressuduku10runsP1.txt
│           │   ├── ressuduku10runsP2.txt
│           │   ├── ressuduku10runsP3.txt
│           │   └── reszebra10runs.txt
│           ├── QuAcq_V7_golomb_latest_allmetrics.ipynb
│           ├── QuAcq_V7_JigSaw_latest_allmetrics.ipynb
│           ├── QuAcq_V7_purdey_latest_allmetrics.ipynb
│           ├── QuAcq_V7_random_latest_allmetrics.ipynb
│           ├── QuAcq_V7_Suduku_latest_allmetrics.ipynb
│           └── QuAcq_V7_Zebra_latest_allmetrics.ipynb
├── QuAcqBERT
│   ├── PyQuAcq_NLP_auto_ordered_allmetrics_countedseparatly
│   │   ├── exact
│   │   │   ├── old
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_sol2_exactlatest.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   └── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── older
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   │   └── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_sol2_exact.ipynb
│   │   │   └── Results
│   │   │       ├── old
│   │   │       │   ├── resgolomb10runs10filesFirst5.txt
│   │   │       │   ├── resgolomb10runs10filesFirst5 (x1).txt
│   │   │       │   ├── resgolomb10runs10filesLast5.txt
│   │   │       │   ├── resgolomb10runs10filesLast5 (x1).txt
│   │   │       │   ├── resjigsaw10runs10files0_2.txt
│   │   │       │   ├── resjigsaw10runs10files3_5.txt
│   │   │       │   ├── resjigsaw10runs10files6_7.txt
│   │   │       │   ├── resjigsaw10runs10files8_9.txt
│   │   │       │   ├── respurdey10runs10files.txt
│   │   │       │   ├── ressuduku10runs10files0_2.txt
│   │   │       │   ├── ressuduku10runs10files3_5.txt
│   │   │       │   ├── ressuduku10runs10files6_7.txt
│   │   │       │   ├── ressuduku10runs10files8_9.txt
│   │   │       │   └── reszebra10runs10files.txt
│   │   │       ├── resgolomb10runs10filesFirst5.txt
│   │   │       ├── resgolomb10runs10filesLast5.txt
│   │   │       ├── resjigsaw10runs10files0_2.txt
│   │   │       ├── resjigsaw10runs10files3_5.txt
│   │   │       ├── resjigsaw10runs10files6_7.txt
│   │   │       ├── resjigsaw10runs10files8_9.txt
│   │   │       ├── respurdey10runs10files.txt
│   │   │       ├── resrandom10runs10file0.txt
│   │   │       ├── resrandom10runs10file1.txt
│   │   │       ├── resrandom10runs10files2.txt
│   │   │       ├── resrandom10runs10files3.txt
│   │   │       ├── resrandom10runs10files4.txt
│   │   │       ├── resrandom10runs10files5.txt
│   │   │       ├── resrandom10runs10files6.txt
│   │   │       ├── resrandom10runs10files7.txt
│   │   │       ├── resrandom10runs10files8.txt
│   │   │       ├── resrandom10runs10files9.txt
│   │   │       ├── ressuduku10runs10files0_2.txt
│   │   │       ├── ressuduku10runs10files3_5.txt
│   │   │       ├── ressuduku10runs10files6_7.txt
│   │   │       ├── ressuduku10runs10files8_9.txt
│   │   │       └── reszebra10runs10files.txt
│   │   └── ortools
│   │       ├── old
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   └── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       ├── older
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!! (111).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!! (3).ipynb
│   │       │   ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │       │   └── respurdey10runs10files.txt
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_sol2.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_sol2.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol1.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol2.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_sol3.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_sol2.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_sol2.ipynb
│   │       ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_sol2.ipynb
│   │       └── results
│   │           ├── old
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   └── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           ├── older
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_golomb_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_jigsaw_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!! (111).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_purdey_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_random_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!! (2).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_suduku_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!! (3).ipynb
│   │           │   ├── pyQuAcq_NLP_v3_23classes_latest_zebra_auto_ordered_allmetrics_LatestWorking!!.ipynb
│   │           │   └── respurdey10runs10files.txt
│   │           ├── resgolomb10runs10filessol2.txt
│   │           ├── respurdey10runs10filessol2.txt
│   │           ├── resrandom10runs10filessol2.txt
│   │           ├── ressuduku10runs10files0To3sol2.txt
│   │           ├── ressuduku10runs10files4thFileSol2.txt
│   │           ├── ressuduku10runs10files5thFileSol2.txt
│   │           ├── ressuduku10runs10filesLast4FilesSol2.txt
│   │           └── reszebra10runs10filessol2.txt
│   ├── Scripts
│   │   ├── prepare_TestFiles_NLP_V2_10files.ipynb
│   │   └── read_results_QuAcqBert.ipynb
│   └── testFiles
│       ├── GolombFiles
│       │   ├── constraintsNLPgolomb10.txt
│       │   ├── constraintsNLPgolomb1.txt
│       │   ├── constraintsNLPgolomb2.txt
│       │   ├── constraintsNLPgolomb3.txt
│       │   ├── constraintsNLPgolomb4.txt
│       │   ├── constraintsNLPgolomb5.txt
│       │   ├── constraintsNLPgolomb6.txt
│       │   ├── constraintsNLPgolomb7.txt
│       │   ├── constraintsNLPgolomb8.txt
│       │   ├── constraintsNLPgolomb9.txt
│       │   └── golombCoods.txt
│       ├── JigSawFiles
│       │   ├── constraintsNLPjigsaw10.txt
│       │   ├── constraintsNLPjigsaw1.txt
│       │   ├── constraintsNLPjigsaw2.txt
│       │   ├── constraintsNLPjigsaw3.txt
│       │   ├── constraintsNLPjigsaw4.txt
│       │   ├── constraintsNLPjigsaw5.txt
│       │   ├── constraintsNLPjigsaw6.txt
│       │   ├── constraintsNLPjigsaw7.txt
│       │   ├── constraintsNLPjigsaw8.txt
│       │   ├── constraintsNLPjigsaw9.txt
│       │   └── jigsawCoods.txt
│       ├── PurdeyFiles
│       │   ├── constraintsNLPpurdey10.txt
│       │   ├── constraintsNLPpurdey1.txt
│       │   ├── constraintsNLPpurdey2.txt
│       │   ├── constraintsNLPpurdey3.txt
│       │   ├── constraintsNLPpurdey4.txt
│       │   ├── constraintsNLPpurdey5.txt
│       │   ├── constraintsNLPpurdey6.txt
│       │   ├── constraintsNLPpurdey7.txt
│       │   ├── constraintsNLPpurdey8.txt
│       │   ├── constraintsNLPpurdey9.txt
│       │   └── purdeyCoods.txt
│       ├── SudukuFiles
│       │   ├── constraintsNLPsuduku10.txt
│       │   ├── constraintsNLPsuduku1.txt
│       │   ├── constraintsNLPsuduku2.txt
│       │   ├── constraintsNLPsuduku3.txt
│       │   ├── constraintsNLPsuduku4.txt
│       │   ├── constraintsNLPsuduku5.txt
│       │   ├── constraintsNLPsuduku6.txt
│       │   ├── constraintsNLPsuduku7.txt
│       │   ├── constraintsNLPsuduku8.txt
│       │   ├── constraintsNLPsuduku9.txt
│       │   └── sudukuCoods.txt
│       └── ZebraFiles
│           ├── constraintsNLPzebra10.txt
│           ├── constraintsNLPzebra1.txt
│           ├── constraintsNLPzebra2.txt
│           ├── constraintsNLPzebra3.txt
│           ├── constraintsNLPzebra4.txt
│           ├── constraintsNLPzebra5.txt
│           ├── constraintsNLPzebra6.txt
│           ├── constraintsNLPzebra7.txt
│           ├── constraintsNLPzebra8.txt
│           ├── constraintsNLPzebra9.txt
│           └── zebraCoods.txt
├── Readme.md
```


