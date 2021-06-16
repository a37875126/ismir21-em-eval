# ismir21-embedding-evaluation
Complementary results to the publication "Performance and limitations of audio embeddings for music classification"

## MTG-Jamendo Dataset annotations
The folder [mtg-jamendo-annotations](mtg-jamendo-annotations) contains the annotations generated for the cross-collection external validation section of the project.
The annotations follow 14 different taxonomies and can be linked to the [test-set of the split-0](https://github.com/MTG/mtg-jamendo-dataset/blob/master/data/splits/split-0/autotagging-test.tsv) of the MTG-Jamendo dataset.

## Results
The folder [results](results) contains the metrics obtained by all the models trained for this project.

### Downstream dataset size
The structure of this section is:

`<trial>/<embedding_type>/<downstream_task>/<size>/results_whole`

where `trial` can be 1, 2 or 3 and are repetitions with a different seed number, `embedding_type` is the type of embedding used to train the model, `downstream_task` is the downstream classification task, and `size` is the amount of samples per class used to train the model.

### Combination of embeddings
The structure of this section is:

`<type_of_experiment>/<n_embeddings>/<embedding_types>`

where `type_of_experiment` can be baseline (the ones presented in the paper) or pca-100 with the difference that the pca-100 features are compressed with PCA so that they have a dimensionality of 100. `n_embeddings` is the number of embedding types combined, and `embedding_types` are the types of embeddings used for training separated by two underscores (`__`).


### Cross-collection external validation
We did not perform cross-collection evaluations on the PCA-compressed features as that experiment did not look very promising, so the results are only reported for the baseline models. The structure of this section is:

`<n_embeddings>/<embedding_types>`

### benchmarks on public datasets
The structure of this section is:

`<downstream_task>/<n_embeddings>/<embedding_types>`
