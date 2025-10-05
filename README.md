# SS-JDSC: 単一話者による日本語構音障害音声コーパス / Single-speaker Japanese dysarthric speech corpus

本コーパスは，日本語の構音障害音声認識およびその関連タスクのために設計された，単一話者による読み上げ音声コーパスです．鼻咽腔閉鎖不全に伴う構音障害音声を約15時間分含んでいます．

SS-JDSC is the corpus of Japanese dysarthric speech designed for research on automatic speech recognition and related tasks. 
It provides 15 hours of speech data from a single Japanese male speaker with velopharyngeal insufficiency (VPI).

[サンプル / Sample](xxx)

## ダウンロード / Download
[リンク / Link](xxx) (zip, xx.xx GB)

## コーパスデザイン / Corpus design
本コーパスは 3 つのサブセットから成ります．
- `basic`: 通常音声（[JSUTコーパス BASIC5000](https://sites.google.com/site/shinnosuketakamichi/publication/jsut)）と同じ文を発話．/ Parallel to control speech in [JSUT BASIC5000](https://sites.google.com/site/shinnosuketakamichi/publication/jsut).
- `hard`: 聞き取り困難な音素を含む発話．/ Phoetically confusable utterances.
- `daily`: 日常会話に使われるフレーズを含む発話．/ Daily-use phrases.

音声認識評価のために，それぞれのサブセットについてテストセットリスト(`test_{basic, hard, daily}.txt`)を含んでいます．音声のフォーマットは 44.1 kHz サンプリング周波数, 16bit RIFF WAV 形式です．

For speech recognition evaluation, test set lists for the subsets, `test_{basic, hard, daily}.txt`, are included in the corpus. The audio format is 44.1 kHz-sampled, 16-bit encoded RIFF WAV format.


| サブセット / Subset | カテゴリ / Category | 説明 / Description                               | 発話数 / #utts | 時間長 / Dur. [h] |
| --------- | -------- | --------------------------------- | ------ | -------- |
| Basic     | -        | 通常音声と同じ文 / Parallel to control speech                  | 4,701  | 6.89     |
| Hard      | CF       | 聞き取りづらい音素を含む文 / Phonemic confusion          | 2,094  | 1.84     |
|           | PCS      | 音声的に混同しやすい文 / Phonetically confusable              | 75     | 0.07     |
|           | SUS      | 合文法無意味文 / Semantically unpredictable                     | 73     | 0.09     |
| Daily     | Everyday | 家族や友達との会話 / Chat with family and friends                 | 2,098  | 2.62     |
|           | Research | 研究者との議論 / Discussions with researchers                    | 927    | 1.39     |
|           | Work     | 公共スペースでの会話 / Conversation in public facilities                | 721    | 1.06     |
|           | Emotion  | 感情表現 / Emotion expression and statements                         | 414    | 0.54     |
|           | Others   | 緊急，季節，趣味 / Urgency, seasons, or hobbies                  | 399    | 0.63     |
| 合計 / Total      | -        | -                                 | 11,502 | 15.12    |

## 音声認識（ASR）ベンチマーク / ASR benchmark
本コーパスを使った音声認識実験の結果です．実験の詳細は文献を参照してください．単語誤り率（WER），BERTScore，Human eval. の値は，全てのテストセットリストの結果を平均したものです．

The table lists the results of our ASR experiments. See our paper for the details. Values are aggregated among test set lists for each of WER (word error rate), BERTScore, Human eval. 

| モデル / model | WER | BERTScore | Human eval. |
| -------------- | --- | --------- | ----------- |
| Whisper large v3 (no finetuning) | 0.934 | 0.654 | 1.217 |
| + finetuning (13.0h) | 0.283 | 0.915 | 3.748 |
| + finetuning + LLM | 0.257 | 0.917 | 4.198 |

## 音声認識デモ / ASR demo
<video src="ss-jdsc.mp4" controls="true"></video>

## ライセンス / License
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.ja)

## 引用 / Citation
(TBA)
