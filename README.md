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

```bash
topsisSolve sample.csv "1,1,1,1" "+,-,+,+" "outputFile.csv"
```
