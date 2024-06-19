# Note

```bash
# 下载zip文件 testsuitedatabases.zip

pip install sqlparse nltk -U

# OK
python evaluation.py --gold evaluation_examples/gold.txt --pred evaluation_examples/predict.txt --db database/ --table tables.json --etype all --plug_value
```