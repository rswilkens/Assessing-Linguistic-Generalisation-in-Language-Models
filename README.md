# Assessing-Linguistic-Generalisation-in-Language-Models

This git contains the files related to the article Assessing-Linguistic-Generalisation-in-Language-Models

The "all-eval.xlsx" spreadsheet contains the whole dataset and the validation of the suggestions made by BERTimbau Large.
Columns A to H contain the main elements, and the subsequent columns contain concatenations related to the evaluation, which were used for further analysis.
* Column A: contains a reference to the template that is being used. These templates are related to the 6 different grammatical tests that are mentioned in the paper and to the different types of sentences that were tested.
* Column B: contains the seed that was used in the test instance
* Column C: contains the full tested instance, including the seed and the masked position ([MASK])
* Column D: has the number of tags from DELAF (see paper) that correspond to the form suggested by BERTimbau Large
* Column E: presents BERTimbau Large's suggested replacement for the masked position in the sentence (Column C)
* Column F: contains the confidence score attributed by BERTimbau Large to the suggested replacement for the masked position
* Column G: contains the evaluation made by a linguist, which is either an "s" to indicate that the token on Column E is a good fit in the sentence, or "n" to indicate that it is not a good fit
* Column H: contains comments related to evaluation. These comments are in Portuguese

Multiword Expression Tests (BertMaskMWE.ipynb)
This file includes the MWEs and sentence examples for each MWE, as well as the script to generate and evaluate the MWE, given the context sentence and an MWE component using the Bertimbau Base and Large language models and mBERT.

Grammatical Tests (BertMaskSyntactic.ipynb)
This file includes sentences and templates for sentence creation for each of the syntactic structures studied in the article. The script starts by generating all the possible clues for templates that are manually downloaded and evaluated to remove invalid generations (acceptability evaluation). Finally, the script loads the validated templates and moves to the generation of words. The script includes the parameters for exploring the [CLS] and the [SEP], which are not discussed in the article.
