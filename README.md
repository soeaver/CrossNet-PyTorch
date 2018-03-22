# CrossNet-PyTorch

### Total performance

**1. Our CrossNet**

|  Network|       FLops</br>(M)       |  Params</br>(M) | 224x224</br>top1-err   |   Server  |
| :--------------------------------------: | :----: | :----: | :--------------------: | :-------: |
| crossnet56k5_b64e1g4                     | 472    | 4.06   | 27.51/27.19            | 20-former |
| crossnet74k5_b48e075                     | 485    | 3.84   | 28.10/27.74            | 20-later  |  
| crossnet62k5_b64e1g4                     | 550    | 4.60   | 27.06/26.87            | 70-former |
| crossnet62k5_b64e1g8                     | 470    | 4.09   | 27.70/27.39            | 70-later  |  
| crossnet62k5_b64e1g8_wd3e-5              | 470    | 4.09   | 27.35/27.01            | 30-former |
| crossnet62k5_b64e1g8_lr0.15              | 470    | 4.09   | 28.11/27.65            | 30-later  |
| crossnet62k5_b64e1g8_bs1024              | 470    | 4.09   | 27.63/27.36            | 21-all    |
| crossnet62k5_b64e1g8_pool                | 454    | 4.08   | 28.05/--               | 40-former |
| crossnet62k5_b64e1g8_conv4               | 483    | 4.09   | 27.55/27.15            | 40-later  |
|                                          |        |        |                        |           |
| wd=3e-5                                  |        |        |                        |           |
| crossnet56k5_b64e1g4_1920                | 489    | 5.03   | 26.94/26.70            | 20-former |
| crossnet56k5_b96e05g8                    | 467    | 3.80   | 27.35/--               | 20-later  |
| crossnet56k5_b64e05                      | 444    | 3.81   | 27.50/27.06            | 21-all    |
| crossnet62d2k5_b100e05g10                | 468    | 4.12   | 27.52/--               | 30-former |
| crossnet56k5_b100e05g10                  | 487    | 3.89   | 27.47/--               | 30-later  |
| crossnet47k5_b72e05                      | 469    | 4.02   | 27.68/--               | 40-former |
| crossnet47k5_b72e1g6                     | 463    | 4.02   | --/--                  | 40-later  |
| crossnet56k5_b72e075g3                   | 490    | 4.10   | 27.11/--               | 70-former |
| crossnet65k5_b72e05g2                    | 457    | 3.58   | 27.03/--               | 70-later  |
|                                          |        |        |                        |           |
| crossnet56k5_b64e05_1600_wd2e-5          | 448    | 4.21   | --/--                  | 20-former |
| crossnet56k5_b64e05_1600gpu2             | 448    | 4.21   | --/--                  | 20-later1 |
| crossnet56k5_b64e05_1600gpu2_24conv1     | 442    | 4.21   | --/--                  | 20-later2 |
| crossnet56k5_b64e05_1600                 | 448    | 4.21   | --/--                  | 21-all    |
| crossnet65k5_b48e075_1600                | 438    | 3.98   | --/--                  | 30-former |
| crossnet56k5_b48e075_1600                | 383    | 3.91   | --/--                  | 30-later  |
| crossnet56k5_b64e05_1600_64head          | 474    | 4.22   | --/--                  | 70-former |
| crossnet65k5_b60e05_1600                 | 458    | 4.01   | --/--                  | 70-later  |
