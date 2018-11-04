# mrc-heuristics

The data for ["What Makes Reading Comprehension Questions Easier?"](http://aclweb.org/anthology/D18-1453) (Sugawara et al., EMNLP 2018)


### Easy and Hard subsets for machine reading comprehension datasets

This repository now has easy/hard question ids for the following datasets:

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

### File formatting
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

See the paper for the details.
