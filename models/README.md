# Обученные модели с адаптерами

Модели можно найти по здесь:
https://drive.google.com/drive/folders/1jgp3GvM-jeaynyMh_-PJ337GVVbIedRH?usp=sharing

Для активации адаптеров
```
tokenizer_name ='bert-base-uncased'
tokenizer = BertTokenizer.from_pretrained(tokenizer_name)

lm='/content/drive/MyDrive/Диплом2/Models/2.0'
config = AutoConfig.from_pretrained(lm)

model = AutoModelForMaskedLM.from_pretrained(lm, config=config)
model.set_active_adapters(['mlm_thesis'])
```
