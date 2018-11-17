# mrc-heuristics

The data for ["What Makes Reading Comprehension Questions Easier?"](http://aclweb.org/anthology/D18-1453) (Sugawara et al., EMNLP 2018)


### Easy and Hard subsets for machine reading comprehension datasets

#### Datasets

This repository now has easy/hard question ids and annotation data for the following datasets:

1. SQuAD (v1.1) [Rajpurkar et al., 2016]
2. AddSent [Jia and Liang, 2017]
3. NewsQA [Trischler et al., 2017]
4. TriviaQA (Wikipedia set) [Joshi et al., 2017]
5. QAngaroo (WikiHop) [Welbl et al., 2018]
6. MS MARCO (v2) [Nguyen et al., 2016]
7. NarrativeQA (summary) [Kočiský et al., 2018]
8. MCTest (160 + 500) [Richardson et al., 2013]
9. RACE (middle + high) [Lai et al., 2017]
10. MCScript [Ostermann et al., 2018]
11. ARC Easy [Clark et al., 2018]
12. ARC Challenge [Clark et al., 2018]

#### Easy and hard subsets
A json file consists as follows:

```
{question_id:
  {"f1"/"exact_match"/"rouge_l": [score],
   "predictions": [prediction]
  }
 question_id:
 ...
}
```

The score and prediction are made by the baseline system (BiDAF or GAR).

### Validity and requisite skill annotation

##### Validity
- valid/invalid = 1/0
- multiple/single candidate = 1/0
- unambiguous/ambiguous = 1/0

##### Skills
Multi-labeling. if multiple labels are selected, we used the most bottom label to compute statistics
- 0 = word matching
- 1 = paraphrasing
- 2 = knowledge reasoning
- 3 = meta/whole reasoning
- 4 = math/logical reasoning

##### Multisentence reasoining or not = 1/0
Relations (single-labeling)
- 0 = coreference
- 1 = causal relation
- 2 = spatial temporal
- 3 = none


See the paper for the details.
