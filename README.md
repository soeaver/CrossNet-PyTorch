# CrossNet-PyTorch

### Total performance

**1. Our CrossNet**

|  Network     |       FLops</br>(M)       |  Params</br>(M) | 224x224</br>top1-acc   |   Server  |
| :--------------------------------------: | :----: | :----: | :--------------------: | :-------: |
| crossnet56k5_b64e1g4                     | 472    | 4.06   | --/--                  | 20-former |
| crossnet74k5_b48e075                     | 485    | 3.84   | --/--                  | 20-later  |  
| crossnet62k5_b64e1g4                     | 550    | 4.60   | --/--                  | 70-former |
| crossnet62k5_b64e1g8                     | 470    | 4.09   | --/--                  | 70-later  |  
| crossnet62k5_b64e1g8_wd3e-5              | 470    | 4.09   | --/--                  | 30-former |
| crossnet62k5_b64e1g8_lr0.15              | 470    | 4.09   | --/--                  | 30-later  |
| crossnet62k5_b64e1g8_bs1024              | 470    | 4.09   | --/--                  | 21-all    |
| crossnet62k5_b64e1g8_pool                | 454    | 4.08   | --/--                  | 40-former |
| crossnet62k5_b64e1g8_conv4               | 483    | 4.09   | --/--                  | 40-later  |
|                                          |        |        |                        |
| crossnet62-e64e05g8                      | 234    | 2.72   | --/--                  | 70-later  |
