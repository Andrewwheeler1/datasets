<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="vctk" />
  <meta itemprop="description" content="This CSTR VCTK Corpus includes speech data uttered by 110 English speakers with&#10;various accents. Each speaker reads out about 400 sentences, which were selected&#10;from a newspaper, the rainbow passage and an elicitation paragraph used for the&#10;speech accent archive.&#10;&#10;Note that the &#x27;p315&#x27; text was lost due to a hard disk error.&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;vctk&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/vctk" />
  <meta itemprop="sameAs" content="https://doi.org/10.7488/ds/2645" />
  <meta itemprop="citation" content="@misc{yamagishi2019vctk,&#10;  author={Yamagishi, Junichi and Veaux, Christophe and MacDonald, Kirsten},&#10;  title={{CSTR VCTK Corpus}: English Multi-speaker Corpus for {CSTR} Voice Cloning Toolkit (version 0.92)},&#10;  publisher={University of Edinburgh. The Centre for Speech Technology Research (CSTR)},&#10;  year=2019,&#10;  doi={10.7488/ds/2645},&#10;}" />
</div>

# `vctk`


Note: This dataset has been updated since the last stable release. The new
versions and config marked with
<span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>
are only available in the `tfds-nightly` package.

*   **Description**:

This CSTR VCTK Corpus includes speech data uttered by 110 English speakers with
various accents. Each speaker reads out about 400 sentences, which were selected
from a newspaper, the rainbow passage and an elicitation paragraph used for the
speech accent archive.

Note that the 'p315' text was lost due to a hard disk error.

*   **Homepage**:
    [https://doi.org/10.7488/ds/2645](https://doi.org/10.7488/ds/2645)

*   **Source code**:
    [`tfds.audio.Vctk`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/audio/vctk.py)

*   **Versions**:

    *   `1.0.0`: VCTK release 0.92.0.
    *   **`1.0.1`** (default)
        <span class="material-icons" title="Available only in the tfds-nightly package">nights_stay</span>:
        Fix speech data type with dtype=tf.int16.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
FeaturesDict({
    'accent': ClassLabel(shape=(), dtype=tf.int64, num_classes=13),
    'gender': ClassLabel(shape=(), dtype=tf.int64, num_classes=2),
    'id': tf.string,
    'speaker': ClassLabel(shape=(), dtype=tf.int64, num_classes=110),
    'speech': Audio(shape=(None,), dtype=tf.int16),
    'text': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class        | Shape   | Dtype     | Description
:------ | :----------- | :------ | :-------- | :----------
        | FeaturesDict |         |           |
accent  | ClassLabel   |         | tf.int64  |
gender  | ClassLabel   |         | tf.int64  |
id      | Tensor       |         | tf.string |
speaker | ClassLabel   |         | tf.int64  |
speech  | Audio        | (None,) | tf.int16  |
text    | Text         |         | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('text', 'speech')`

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

*   **Citation**:

```
@misc{yamagishi2019vctk,
  author={Yamagishi, Junichi and Veaux, Christophe and MacDonald, Kirsten},
  title={{CSTR VCTK Corpus}: English Multi-speaker Corpus for {CSTR} Voice Cloning Toolkit (version 0.92)},
  publisher={University of Edinburgh. The Centre for Speech Technology Research (CSTR)},
  year=2019,
  doi={10.7488/ds/2645},
}
```


## vctk/mic1 (default config)

*   **Config description**: Audio recorded using an omni-directional microphone
    (DPA 4035). Contains very low frequency noises.

    ```
          This is the same audio released in previous versions of VCTK:
          https://doi.org/10.7488/ds/1994
    ```

## vctk/mic2

*   **Config description**: Audio recorded using a small diaphragm condenser
    microphone with very wide bandwidth (Sennheiser MKH 800).

    ```
          Two speakers, p280 and p315 had technical issues of the audio
          recordings using MKH 800.
    ```
