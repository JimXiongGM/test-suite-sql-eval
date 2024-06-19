# Note

```bash
# 下载zip文件 testsuitedatabases.zip

pip install sqlparse nltk -U

# OK
# --plug_value: If your system does NOT predict values in the SQL queries, you should add the --plug value flag
# 什么意思？？
python evaluation.py --gold spider_dataset/dev_gold.sql --pred DAIL-SQL-res/DAIL-SQL+GPT-4.txt --db spider_dataset/database/ --table spider_dataset/tables.json --etype all
```

DAIL-SQL 的各种结果
```bash
# spider dev: 1034 cases
# Execution Scores: 0.8307; Exact Match Scores: 0.7001
python evaluation.py --gold spider_dataset/dev_gold.sql --pred DAIL-SQL-res/DAIL-SQL+GPT-4.txt --db spider_dataset/database/ --table spider_dataset/tables.json --etype all

# Execution Scores: 0.8355; Exact Match Scores: 0.6866
python evaluation.py --gold spider_dataset/dev_gold.sql --pred DAIL-SQL-res/DAIL-SQL+GPT-4+self-consistency.txt --db spider_dataset/database/ --table spider_dataset/tables.json --etype all

# Execution Scores: 0.8094; Exact Match Scores: 0.7707
python evaluation.py --gold spider_dataset/dev_gold.sql --pred DAIL-SQL-res/graphix_result.txt --db spider_dataset/database/ --table spider_dataset/tables.json --etype all

# BIRD dev: 1534 cases
# 跑不通！！
```