Rx Power, Fresnel Radius Caculator
==================================

You can check it at: https://bit.ly/45ov7em

## Product Data in CSV

- FormatVersion: String: '0.1a', must be placed at the cell "$A$1" and "$B$1".
- ProdName: String: Required. Product name.
- pProdName: String or null: Parent product name, use in GUI.
- ProdType: Required. Literal['D', 'A', 'C', 'O']
   + D: Device
   + A: Antenna
   + C: Cable
   + O: Other
- FreqL: Float or null: lowest frequency to be used in MHz
- FreqH: Float or null: hightest frequency to be used in MHz
- Value: Float: Required. maximum value of when ProductType is:
   + 'antenna', Value must be a gain in dBi.
   + 'cable', Value must be a loss in dB.
   + 'other', Value must be a loss in dB.
   + 'device', if the antenna is integrated, Value must be a gain in dBi.
- Region: String or null: alpha-2 country code.
- Example in CSV is [here](https://raw.githubusercontent.com/tanupoo/radioprop-tools/main/prod_list-sample.csv)
- Example in Excel.

```
  |        A         |    B      |    C     |   D   |   E   |  F  |  G   |
 1| FormatVersion    | 0.1a      |          |       |       |     |      |
 2| ProdName         | pProdName | ProdType | FreqL | FreqH |Value|Region|
  |------------------|-----------|----------|-------|-------|-----|------|
 3|C9130AXI          |           |    D     | 2412  | 2472  | 23  |      |
 4|C9130AXI          |           |    D     | 5160  | 5720  | 26  |      |
 5|P-LTEA-LA         | IR1101-K9 |    D     | 700   | 3600  | 23  | JP   |
 6|5G-ANTM-SMA-D     | P-LTEA-LA |    A     | 617   | 960   | 1.2 |      |
 7|5G-ANTM-SMA-D     | P-LTEA-LA |    A     | 1430  | 3500  | 2.5 |      |
 8|5G-ANTM-SMA-D     | P-LTEA-LA |    A     | 3500  | 6000  | 5.5 |      |
 9|P-LPWA-900        | IR1101-K9 |    D     | 920   | 928   | 13  |      |
10|IXM-LPWA-900-16-K9|           |    D     | 920   | 928   | 11  | JP   |
11|ANT-LPWA-DB-O-N-5 |           |    A     |       |       | 4   |      |
12|CAB-L400-20-N-N   |           |    C     |       |       | 1   |      |
13|ACC-LA-H-NM-NF    |           |    O     |       |       | .5  |      |
```

