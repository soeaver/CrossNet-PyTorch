# CrossNet-PyTorch

### Total performance

**1. Our CrossNet**

|  Network|       FLops</br>(M)       |  Params</br>(M) | 224x224</br>top1-err   |   Server  |
| :--------------------------------------: | :----: | :----: | :--------------------: | :-------: |
| crossnet56k5_b64e1g4                     | 472    | 4.06   | 27.51/27.19            | 20-former |
| crossnet74k5_b48e075                     | 485    | 3.84   | 28.10/27.74            | 20-later  |  
| crossnet62k5_b64e1g4                     | 550    | 4.60   | 27.06/26.87            | 70-former |
| crossnet62k5_b64e1g8                     | 470    | 4.09   | 27.70/27.39            | 70-later  |  
| crossnet62k5_b64e1g8_wd3e-5              | 470    | 4.09   | --/--                  | 30-former |
| crossnet62k5_b64e1g8_lr0.15              | 470    | 4.09   | 28.11/27.65            | 30-later  |
| crossnet62k5_b64e1g8_bs1024              | 470    | 4.09   | 27.63/27.36            | 21-all    |
| crossnet62k5_b64e1g8_pool                | 454    | 4.08   | 28.05/--               | 40-former |
| crossnet62k5_b64e1g8_conv4               | 483    | 4.09   | 27.55/27.15            | 40-later  |
|                                          |        |        |                        |
| crossnet62-e64e05g8                      | 234    | 2.72   | --/--                  | 70-later  |
