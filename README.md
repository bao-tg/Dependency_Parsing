# Transition-based dependency parsing in NLP

# Acknowledgement
This project have used the implemented configurations from the course CS224n: Natural Language Processing with Deep Learning

# Description
Dependency parsing in NLP analyzes sentence structure by establishing grammatical relations between words, unlike traditional constituency-based parsing. It provides a direct representation of syntactic relationships, crucial for tasks like information extraction and machine translation.

Given the importance of dependency parsing, In this project, we aim to implement two key dependency parsing algorithms: Transition-Based Dependency Parsing and Graph-Based Dependency Parsing.

In this repository, I will implement the basic architect neural network parser for the class of parsing algorithm, traision-based dependency parsing

# Requirements

```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip3 install tqdm 
```

# Getting started
```bash
git clone https://github.com/bao-tg/Dependency_Parsing
```

```bash
cd Dependency_Parsing
```

```bash
python run.py
```

# Train - Valid - Test on different dataset

Train on the entire corpus, change the parameter debug on the run.py file (line 125)

The default data for the project is VnDT data, if you want to train - test the data on the Universal Dependencies dataset, you need to change the following settings (In the parser_utils.py):
+ Path to the dataset, line 32 - 37
+ Change open(in_file, 'r', encoding = 'utf-8') to open(in_file), line 289, 372.
+ Erase the two conditional commands, line 374, 375.
+ Change the dimension from line 377 so that it is identical to the dimension of embedddings data (in this case, we change 100 to 300).

# Dataset
+ VnDT: https://github.com/datquocnguyen/VnDT
+ Universal Dependencies: https://github.com/UniversalDependencies

# References
[1] Universal Dependencies. (2024) \text{UD-Afrikaans-AfriBooms} [GitHub repository]

[2] Manning, C. D. (2024) CS224n: Natural Language Processing with Deep Learning. Stanford University. Available at: https://cs224n.stanford.edu/

[3] Nguyen, A.T., Dao, M.H., \ \& Nguyen, D.Q. \ (2020) A Pilot Study of Text-to-SQL Semantic Parsing for Vietnamese. In {\it Findings of the Association for Computational Linguistics: EMNLP 2020}, pp. 4079--4085.

[4] Fares, M., Kutuzov, A., Oepen, S., \ \& Velldal, E. \ (2017) Word vectors, reuse, and replicability: Towards a community repository of large-text resources. In {\it Proceedings of the 21st Nordic Conference on Computational Linguistics}, pp. 271--276. Gothenburg, Sweden: Association for Computational Linguistics.

[5] Chen, D. \& Manning, C. (2014) A Fast and Accurate Dependency Parser using Neural Networks. In Proceedings of the 2014 Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 740–750. Doha, Qatar: Association for Computational Linguistics. Available: https://aclanthology.org/D14-1082, DOI: 10.3115/v1/D14-1082
