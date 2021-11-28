# BERT

## Как пользоваться

### bert.ipynb

- открывать в **jupyter notebook** (не github, не colab)
    - в коде присутствуют ячейки типа `Code`, который github совсем недавно решил не отрисовывать, а colab ругается на тип этой ячейки
- ячейки типа Code — долгие по времени, поэтому рядом с ними я подгружаю результат исполнения этой ячейки с диска

### logs

- отдельно смотреть pretraining / finetuning: 
    - `tensorboard --logdir logs/pretraining`
    - `tensorboard --logdir logs/finetuning`
    - потому что во вкладке hparams иначе перемешиваются модели
- когда находитесь на вкладке scalars введите фильтр `^((?!hyperparams).)*$`, чтобы убрать гиперпараметры
- гиперпараметры смотреть отдельно во вкладке hparams, включите параметры:
    - pretraining: `hidden_size`, `num_hidden_layers`, `batch_size`, `{init, peak, final}_lr`, `last_epoch`, все метрики
    - finetuning: `hidden_size`, `num_hidden_layers`, `{init, peak, final}_lr`, все метрики
