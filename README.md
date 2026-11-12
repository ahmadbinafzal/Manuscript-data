# Case study data: three-stage resilience planning with mobile energy storage

Case study data for the IEEE 33-bus and IEEE 123-bus distribution systems used in the paper "Adaptive Three-Stage Resilience Planning for Distribution Systems with Pre-Event Resource Provisioning and Mobile Energy Storage Coordination", submitted to the *Journal of Energy Storage* (manuscript EST-D-26-07142).

## Files

| File | Contents | Paper |
|---|---|---|
| `Input_data_and_parameters.xlsx` | cost parameters, model parameters, hourly electricity price, hourly load of both systems, references | Section 3, Table 4 |
| `Extreme_event_scenarios.xlsx` | scenario-generation settings, the three hurricane paths and the damage scenarios used in the case studies (failed lines) | Sections 2.1, 3.1 |

The first sheet of each workbook (`Read_me`) explains its sheets.

## Input_data_and_parameters.xlsx

| Sheet | Contents |
|---|---|
| `Cost_parameters` | cost parameters of Table 4 and their sources |
| `Model_parameters` | network, WT, MES, crew, hardening, repair and BaseCase1 BESS parameters for both systems |
| `Electricity_price` | hourly purchase price at the substation and export price (10 % of the purchase price), USD/kWh |
| `Load_IEEE33_P_kW`, `Load_IEEE33_Q_kVAr` | hourly active and reactive demand of the 32 load buses |
| `Load_IEEE123_P_kW`, `Load_IEEE123_Q_kVAr` | hourly active and reactive demand of the 85 load buses |
| `References` | references of the parameter sources |

## Extreme_event_scenarios.xlsx

| Sheet | Contents |
|---|---|
| `Event_parameters` | wind-field, fragility, Monte Carlo, severity-index, clustering and Weibull settings |
| `Paths` | the three hurricane paths (Extreme Events 1-3): storm wind speed, category, MES and crew price factors, path weight |
| `Scenarios_IEEE33`, `Scenarios_IEEE123` | 12 scenarios per system: for each path, the estimated worst-case damage scenario (Stage 2, Stage 3F) and the three damage realizations R1-R3 (Stage 3R, weight 1/3 each), with the failed lines, wind speed on the failed lines, disconnected load and severity index |

## Conventions

- Failed lines are written as `from bus-to bus` (e.g. `6-26`), with the bus numbers of Fig. 4 (IEEE 33-bus) and Fig. 8 (IEEE 123-bus) in the paper.
- Disconnected load and severity index are pre-restoration values (normally closed network, before hardening,
  reconfiguration, repair or MES dispatch).
- Costs in USD, energy in kWh, power in kW, time step 1 h, one operating day = 24 h.

## Citation

If you use these data, please cite the paper.
