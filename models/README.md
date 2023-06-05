# Обученные модели с адаптерами
Для активации адаптеров
```
tokenizer_name ='bert-base-uncased'
tokenizer = BertTokenizer.from_pretrained(tokenizer_name)

lm='/content/drive/MyDrive/Диплом2/Models/2.0'
config = AutoConfig.from_pretrained(lm)

model = AutoModelForMaskedLM.from_pretrained(lm, config=config)
model.set_active_adapters(['mlm_thesis'])
```
