# rbma-fakes

Imaginary transcripts of [Red Bull Music Academy](https://www.redbullmusicacademy.com/) (RBMA) lectures, generated using [GPT-2](https://github.com/openai/gpt-2) via [gpt-2-simple](https://github.com/minimaxir/gpt-2-simple). The medium (355M parameter) model was fine-tuned using actual RBMA lectures (~500 transcripts, ~20MB of text) for 1,000 steps.

There are a selection of dumps (lol) of transcripts for each "temperature" - the higher the temperature, the weirder (and less syntactically correct) the lectures are.

- `temp_0_7`: Normal and syntactically correct
- `temp_0_7_bellerin`: Normal and syntactically correct but about Héctor Bellerín
- `temp_1_0`: Wilder and less syntactically correct
- `temp_1_3`: Very extremely wild O_o

## Get the text corpus

The actual transcripts are available in plain-text format within the [rbma-lectures](https://github.com/ewenme/rbma-lectures) repo, taken from the [RBMA lectures mini-site](https://www.redbullmusicacademy.com/lectures) on 3rd November, 2019. 

## Retrain

The files within the `data/` subdirectory of the `rbma-lectures` repo were appended into a single .txt file and used to retrain the model with `gpt-2-simple` using a GPU via a copy of [this Colaboratory notebook](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce). (I haven't shared the retrained model because it is very large). The same notebook was used to generate the new transcripts and then downloaded locally.