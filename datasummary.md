## Dataset summary

This dataset contains monthly average river water quality measurements from multiple upstream stations (1-7). The goal is to predict the water quality value at the target station (station 8) using measurements from upstream stations.

**Target column**
- `target`: the value to predict for the target station.

**Feature groups (per station)**
- `O2_1` ... `O2_7`: dissolved oxygen.
- `NH4_1` ... `NH4_7`: ammonium ions.
- `NO2_1` ... `NO2_7`: nitrite ions.
- `NO3_1` ... `NO3_7`: nitrate ions.
- `BOD5_1` ... `BOD5_7`: biochemical oxygen demand (5 days).

**Identifier**
- `Id`: record identifier (not a predictive feature).

## Column name cleanup

The raw CSV has inconsistent spacing in column names. In notebooks I normalize names by:
- trimming whitespace,
- converting to lowercase,
- removing non-alphanumeric characters except `_`.

This produces a consistent schema such as `o2_1`, `nh4_3`, `bod5_7`, and keeps `target` as the prediction label.
