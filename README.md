# Question-Answering-with-Transformers :crystal_ball: :green_book:
©Riccardo Paolini @Davide Femia @Alessandro D’Amico ©Sfarzo El Husseini

In this work we address the problem of Conversational Question Answering, with reference to the [CoQA dataset introduced by Stanford University in (Reddy et al., 2018)](https://stanfordnlp.github.io/coqa/). One of the major challenges of this tasks is the management of the conversation history to answer the current question. 
We propose a solution based on Transformers such as BERTTiny and DistilRoBERTa.
In particular, our architectures consist of two networks, the first deals with the rationale (the sentence which contains the answer) extraction, while the latter identifies the correct answer and reformulates it (see figure below).

![](./img/span_encoderdecoder.jfif "span extractor + encoder/decoder")


## Models
- BERTTiny (``prajjwal1/bert-tiny``)
- DistilRoBERTa (```distilroberta-base```)

## Tested configurations
Two main configurations were experimented

- *Not* Considering the history of the conversation    
- Considering the history of the conversation (4 previous dialogues)

These models were tested both on the test set and validation set, obtaining the following results:


<table class="tg">
<thead>
  <tr>
    <th class="tg-cly1" rowspan="2">Model</th>
    <th class="tg-cly1" rowspan="2">History</th>
    <th class="tg-cly1" colspan="1">SQUAD-F1</th>
  </tr>
  <tr>
    <th class="tg-cly1">Test</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-cly1" rowspan="4">BERTTiny</td>
    <td class="tg-cly1">YES</td>
    <td class="tg-cly1">83.94%</td>
  </tr>
  <tr>
    <td class="tg-cly1">NO</td>
    <td class="tg-cly1">19.88%</td>
  </tr>
  <tr>
    <td class="tg-cly1">WH</td>
    <td class="tg-cly1">14.12%</td>
  </tr>
  <tr>
    <td class="tg-cly1">MC</td>
    <td class="tg-cly1">17.39%</td>
  </tr>
  <tr>
    <td class="tg-cly1" rowspan="4">DistilRoBERTa</td>
    <td class="tg-cly1">YES</td>
    <td class="tg-cly1">68.94%</td>
  </tr>
  <tr>
    <td class="tg-cly1">NO</td>
    <td class="tg-cly1">74.59%</td>
  </tr>
    <tr>
    <td class="tg-cly1">WH</td>
    <td class="tg-cly1">44.95%</td>
  </tr>
  <tr>
    <td class="tg-cly1">MC</td>
    <td class="tg-cly1">33.30%</td>
  </tr>
</tbody>
</table>
