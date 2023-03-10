# Topsis

Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS)

MCDM for algorithm selection
Multiple-criteria decision methods (MCDM) can help decisions with more than one criterion. These methods can be applied to several business problems like supplier evaluation, project prioritizing, and raw material selection. They also can be used in personal situations like consumer goods choice. This work aims to use a multicriteria decision method to help on algorithm selection.

It is a multi-criteria decision analysis method that is based on the concept that the chosen alternative should have the shortest geometric distance to the Positive Ideal Solution (PIS) and the longest geometric solution from the Negative Ideal Solution (NIS).

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install topsis_102003313.

```bash
pip install topsis-102003313
```

## Usage

Enter csv filename followed by _.csv_ extentsion, then enter the _weights_ vector with vector values separated by commas, followed by the _impacts_ vector with comma separated signs _(+,-)_, and lastly the _outputFileName_.

-Input and output file format should be .CSV

-First column in the input file should be the object name

-Input file must have at least 2 criteria, and all criterion values should be numeric

-Weights must be numeric and comma-separated. For example, 0.25,0.25,1.0,0.25 or "0.25,0.25,1.0,0.25".

-Impacts must be comma-separated with + for criteria that are to be maximised, and - for criteria that are to be minimised.

-For example, +,-,+,- or "+, -, +, -"

## Example

Consider **sample.csv**:
|Model|Correlation|R2|RMSE|Accuracy|
|---|---|---|---|---|
|M1|0.79|0.62|1.25|60.89|
|M2|0.66|0.44|2.89|63.07|
|M3|0.56|0.31|1.57|62.87|
|M4|0.82|0.67|2.68|70.19|
|M5|0.75|0.56|1.3|80.39|

If we run the following command:

```bash
python topsis.py sample.csv "1,1,1,1" "+,-,+,+" outputFile.csv
```

We get a file named **outputFile.csv** in the directory in addition to  two new columns containing the TOPSIS score and the Rank of each object:
|Model|Correlation|R2|RMSE|Accuracy|TOPSIS Score|Rank|
|---|---|---|---|---|---|---|
|M1|0.79|0.62|1.25|60.89|0.7722097345612788|2.0|
|M2|0.66|0.44|2.89|63.07|0.22559875426413367|5.0|
|M3|0.56|0.31|1.57|62.87|0.43889731728018605|4.0|
|M4|0.82|0.67|2.68|70.19|0.5238778712729114|3.0|
|M5|0.75|0.56|1.3|80.39|0.8113887082429979|1.0|

## License

MIT
