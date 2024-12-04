# PARIKSHA: A Large-Scale Investigation of Human-LLM Evaluator Agreement on Multilingual and Multi-Cultural Data

**Official Repository for ["PARIKSHA: A Large-Scale Investigation of Human-LLM Evaluator Agreement on Multilingual and Multi-Cultural Data"](https://aclanthology.org/2024.emnlp-main.451/) (Presented at EMNLP 2024)**

## Abstract
Evaluation of multilingual Large Language Models (LLMs) is challenging due to a variety of factors – the lack of benchmarks with sufficient linguistic diversity, contamination of popular benchmarks into LLM pre-training data and the lack of local, cultural nuances in translated benchmarks. In this work, we study human and LLM-based evaluation in a multilingual, multi-cultural setting. We evaluate 30 models across 10 Indic languages by conducting 90K human evaluations and 30K LLM-based evaluations and find that models such as GPT-4o and Llama-3 70B consistently perform best for most Indic languages. We build leaderboards for two evaluation settings - pairwise comparison and direct assessment and analyse the agreement between humans and LLMs. We find that humans and LLMs agree fairly well in the pairwise setting but the agreement drops for direct assessment evaluation especially for languages such as Bengali and Odia. We also check for various biases in human and LLM-based evaluation and find evidence of self-bias in the GPT-based evaluator. Our work presents a significant step towards scaling up multilingual evaluation of LLMs.

## Directory Structure
```bash
.
├── CODE_OF_CONDUCT.md
├── LICENSE
├── README.md
├── SECURITY.md
├── SUPPORT.md
├── gpt_eval
│   └── outputs
│       └── round1
│           ├── individual
│           │   ├── hallucinations
│           │   │   ├── individual_bengali.json
│           │   │   ├── individual_gujarati.json
│           │   │   ├── individual_hindi.json
│           │   │   ├── individual_kannada.json
│           │   │   ├── individual_malayalam.json
│           │   │   ├── individual_marathi.json
│           │   │   ├── individual_odia.json
│           │   │   ├── individual_punjabi.json
│           │   │   ├── individual_tamil.json
│           │   │   └── individual_telugu.json
│           │   ├── linguistic_acceptability
│           │   │   ├── individual_bengali.json
│           │   │   ├── individual_gujarati.json
│           │   │   ├── individual_hindi.json
│           │   │   ├── individual_kannada.json
│           │   │   ├── individual_malayalam.json
│           │   │   ├── individual_marathi.json
│           │   │   ├── individual_odia.json
│           │   │   ├── individual_punjabi.json
│           │   │   ├── individual_tamil.json
│           │   │   └── individual_telugu.json
│           │   └── task_quality
│           │       ├── individual_bengali.json
│           │       ├── individual_gujarati.json
│           │       ├── individual_hindi.json
│           │       ├── individual_kannada.json
│           │       ├── individual_malayalam.json
│           │       ├── individual_marathi.json
│           │       ├── individual_odia.json
│           │       ├── individual_punjabi.json
│           │       ├── individual_tamil.json
│           │       └── individual_telugu.json
│           └── pairwise
│               ├── battle_outcomes_bengali.json
│               ├── battle_outcomes_gujarati.json
│               ├── battle_outcomes_hindi.json
│               ├── battle_outcomes_kannada.json
│               ├── battle_outcomes_malayalam.json
│               ├── battle_outcomes_marathi.json
│               ├── battle_outcomes_odia.json
│               ├── battle_outcomes_punjabi.json
│               ├── battle_outcomes_tamil.json
│               └── battle_outcomes_telugu.json
├── karya_eval
│   └── round1
│       ├── final_battle_outcomes.csv
│       ├── individual
│       │   ├── bengali_ratings_output_indi.tsv
│       │   ├── gujarati_ratings_output_indi_just.tsv
│       │   ├── hindi_ratings_output_indi_just.tsv
│       │   ├── kannada_ratings_output_indi.tsv
│       │   ├── malayalam_ratings_output_indi_just.tsv
│       │   ├── marathi_ratings_output_indi_just.tsv
│       │   ├── odia_ratings_output_indi.tsv
│       │   ├── punjabi_ratings_output_indi_just.tsv
│       │   ├── tamil_ratings_output_indi_just.tsv
│       │   └── telugu_ratings_output_indi.tsv
│       └── pairwise
│           ├── bengali_pairwise_ratings.tsv
│           ├── gujarati_pairwise_ratings.tsv
│           ├── hindi_pairwise_ratings.tsv
│           ├── kannada_pairwise_ratings.tsv
│           ├── malayalam_pairwise_ratings.tsv
│           ├── marathi_pairwise_ratings.tsv
│           ├── odia_pairwise_ratings.tsv
│           ├── punjabi_pairwise_ratings.tsv
│           ├── tamil_pairwise_ratings.tsv
│           └── telugu_pairwise_ratings.tsv
├── outputs
│   └── round1
│       └── formatted
│           ├── output_bengali.json
│           ├── output_gujarati.json
│           ├── output_hindi.json
│           ├── output_kannada.json
│           ├── output_malayalam.json
│           ├── output_marathi.json
│           ├── output_odia.json
│           ├── output_punjabi.json
│           ├── output_tamil.json
│           └── output_telugu.json
├── pairings
│   └── round1
│       ├── llm_eval
│       │   ├── bengali_pairings.json
│       │   ├── gujarati_pairings.json
│       │   ├── hindi_pairings.json
│       │   ├── kannada_pairings.json
│       │   ├── malayalam_pairings.json
│       │   ├── marathi_pairings.json
│       │   ├── odia_pairings.json
│       │   ├── punjabi_pairings.json
│       │   ├── tamil_pairings.json
│       │   └── telugu_pairings.json
│       └── new_karya_eval
│           ├── bengali
│           │   ├── bengali_pairings_1.json
│           │   ├── bengali_pairings_2.json
│           │   ├── bengali_pairings_3.json
│           │   ├── bengali_pairings_4.json
│           │   ├── bengali_pairings_5.json
│           │   ├── bengali_pairings_6.json
│           │   ├── bengali_pairings_7.json
│           │   ├── bengali_pairings_8.json
│           │   └── bengali_pairings_9.json
│           ├── gujarati
│           │   ├── gujarati_pairings_1.json
│           │   ├── gujarati_pairings_2.json
│           │   ├── gujarati_pairings_3.json
│           │   ├── gujarati_pairings_4.json
│           │   └── gujarati_pairings_5.json
│           ├── hindi
│           │   ├── hindi_pairings_1.json
│           │   ├── hindi_pairings_2.json
│           │   ├── hindi_pairings_3.json
│           │   ├── hindi_pairings_4.json
│           │   ├── hindi_pairings_5.json
│           │   ├── hindi_pairings_6.json
│           │   ├── hindi_pairings_7.json
│           │   ├── hindi_pairings_8.json
│           │   └── hindi_pairings_9.json
│           ├── kannada
│           │   ├── kannada_pairings_1.json
│           │   ├── kannada_pairings_2.json
│           │   ├── kannada_pairings_3.json
│           │   ├── kannada_pairings_4.json
│           │   └── kannada_pairings_5.json
│           ├── malayalam
│           │   ├── malayalam_pairings_1.json
│           │   ├── malayalam_pairings_2.json
│           │   ├── malayalam_pairings_3.json
│           │   ├── malayalam_pairings_4.json
│           │   └── malayalam_pairings_5.json
│           ├── marathi
│           │   ├── marathi_pairings_1.json
│           │   ├── marathi_pairings_2.json
│           │   ├── marathi_pairings_3.json
│           │   ├── marathi_pairings_4.json
│           │   ├── marathi_pairings_5.json
│           │   ├── marathi_pairings_6.json
│           │   └── marathi_pairings_7.json
│           ├── odia
│           │   ├── odia_pairings_1.json
│           │   ├── odia_pairings_2.json
│           │   ├── odia_pairings_3.json
│           │   ├── odia_pairings_4.json
│           │   └── odia_pairings_5.json
│           ├── punjabi
│           │   ├── punjabi_pairings_1.json
│           │   ├── punjabi_pairings_2.json
│           │   ├── punjabi_pairings_3.json
│           │   ├── punjabi_pairings_4.json
│           │   └── punjabi_pairings_5.json
│           ├── tamil
│           │   ├── tamil_pairings_1.json
│           │   ├── tamil_pairings_2.json
│           │   ├── tamil_pairings_3.json
│           │   ├── tamil_pairings_4.json
│           │   └── tamil_pairings_5.json
│           └── telugu
│               ├── telugu_pairings_1.json
│               ├── telugu_pairings_2.json
│               ├── telugu_pairings_3.json
│               ├── telugu_pairings_4.json
│               ├── telugu_pairings_5.json
│               ├── telugu_pairings_6.json
│               ├── telugu_pairings_7.json
│               ├── telugu_pairings_8.json
│               └── telugu_pairings_9.json
├── prompts
│   ├── prompts_round1.json
│   └── system_prompts.json
└── results
    └── round1
        ├── final_battle_results.csv
        └── final_individual_results.json
```

## Dataset
- In this repository, we release the model pairings, battle outcomes, LLM-evaluation scores and Human-Evaluation scores. The metric-wise direct assessment scores are available in the `gpt_eval/outputs/round1/individual` directory. Similarly, the pairwise results are available in `gpt_eval/outputs/round1/pairwise`. 
- The `outputs/round1/formatted` directory contains the generations of all the evaluated models for the given prompts. 
- The `karya_eval/round1` directory contains the human-evaluations of the selected prompts and models 
- The **collated** list of all evaluations and prompts is available in the `results/round1` folder and `karya_eval/round1/final_battle_outcomes.csv` file. 
- All our prompts are detailed in the `prompts` directory.

## Note
The Human Evaluations and Prompts were done by [Karya](https://www.karya.in/) and open-sourced on their [repository](https://github.com/karya-inc/pariksha). In our release, we join them with the corresponding LLM generations and evaluations as a single comprehensive list.

## Citation
In you use this dataset, please cite our work,
```bibtex
@inproceedings{watts-etal-2024-pariksha,
    title = "{PARIKSHA}: A Large-Scale Investigation of Human-{LLM} Evaluator Agreement on Multilingual and Multi-Cultural Data",
    author = "Watts, Ishaan  and
      Gumma, Varun  and
      Yadavalli, Aditya  and
      Seshadri, Vivek  and
      Swaminathan, Manohar  and
      Sitaram, Sunayana",
    editor = "Al-Onaizan, Yaser  and
      Bansal, Mohit  and
      Chen, Yun-Nung",
    booktitle = "Proceedings of the 2024 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2024",
    address = "Miami, Florida, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.emnlp-main.451",
    doi = "10.18653/v1/2024.emnlp-main.451",
    pages = "7900--7932",
    abstract = "Evaluation of multilingual Large Language Models (LLMs) is challenging due to a variety of factors {--} the lack of benchmarks with sufficient linguistic diversity, contamination of popular benchmarks into LLM pre-training data and the lack of local, cultural nuances in translated benchmarks. In this work, we study human and LLM-based evaluation in a multilingual, multi-cultural setting. We evaluate 30 models across 10 Indic languages by conducting 90K human evaluations and 30K LLM-based evaluations and find that models such as GPT-4o and Llama-3 70B consistently perform best for most Indic languages. We build leaderboards for two evaluation settings - pairwise comparison and direct assessment and analyse the agreement between humans and LLMs. We find that humans and LLMs agree fairly well in the pairwise setting but the agreement drops for direct assessment evaluation especially for languages such as Bengali and Odia. We also check for various biases in human and LLM-based evaluation and find evidence of self-bias in the GPT-based evaluator. Our work presents a significant step towards scaling up multilingual evaluation of LLMs.",
}
```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.


## Privacy

You can read more about Microsoft's privacy statement [here](https://go.microsoft.com/fwlink/?LinkId=521839).
