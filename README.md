# biaffineparser: Deep Biaffine Attention Dependency Parser

biaffineparser is chainer implementation for Deep Biaffine Attention for Neural Dependency Parsing.

## Installation

biaffineparser works on Python3 and requires chainer, numpy and teras.

```sh
$ git clone https://github.com/chantera/biaffineparser
$ cd biaffineparser
$ pip install -r requirements.txt
```

## Usage

### Training

```sh
usage: parser.py train [-h] [--batchsize BATCH_SIZE] [--embedfile EMBED_FILE]
                       [--embedsize EMBED_SIZE] [--epoch N_EPOCH] [--gpu GPU]
                       [--lr LR] [--model MODEL_PARAMS] [--out SAVE_TO]
                       --trainfile TRAIN_FILE [--validfile TEST_FILE]

optional arguments:
  -h, --help            show this help message and exit
  --batchsize BATCH_SIZE, -b BATCH_SIZE
                        Number of examples in each mini-batch (default: 32)
  --embedfile EMBED_FILE
                        Pretrained word embedding file (default: None)
  --embedsize EMBED_SIZE
                        Size of embeddings (default: 100)
  --epoch N_EPOCH, -e N_EPOCH
                        Number of sweeps over the dataset to train (default:
                        20)
  --gpu GPU, -g GPU     GPU ID (negative value indicates CPU) (default: -1)
  --lr LR               Learning Rate (default: 0.002)
  --model MODEL_PARAMS  Model hyperparameter (default: {})
  --out SAVE_TO         Save model to the specified directory (default: None)
  --trainfile TRAIN_FILE
                        training data file (default: None)
  --validfile TEST_FILE
                        validation data file (default: None)
```

### Testing

```sh
usage: parser.py test [-h] [--decode] [--gpu GPU] --modelfile MODEL_FILE
                      --targetfile TARGET_FILE

optional arguments:
  -h, --help            show this help message and exit
  --decode              Print decoded results (default: False)
  --gpu GPU, -g GPU     GPU ID (negative value indicates CPU) (default: -1)
  --modelfile MODEL_FILE
                        Trained model archive file (default: None)
  --targetfile TARGET_FILE
                        Decoding target data file (default: None)
```

## References

  - Dozat, T., Manning, C. D., 2016. Deep Biaffine Attention for Neural Dependency Parsing. arXiv preprint arXiv:1611.01734. <https://arxiv.org/abs/1611.01734>

License
----
Apache License Version 2.0

&copy; Copyright 2017 Teranishi Hiroki

