# CrossNet-PyTorch

### Total performance

Samsung-S7e (SnapDragon820 on ncnn)

|  Models |       FLops</br>(M)    |  Params</br>(M) | 224x224</br>top1-err   |   CPU Time</br>(Multi-Threads)  |
| :------------------------------: | :----: | :----: | :--------------------: | :-------: |
| MobileNet-v1                     | 569    | 4.24   | 70.9                   | 102ms |
| MobileNet-v2                     | **300**    | 3.47   | 71.7                   | **77ms**  |
| CrossNet (ours)                  | 309    | **3.28**   | **72.2**                   | 84ms  |

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
| crossnet47k5_b72e1g6                     | 463    | 4.02   | 27.44/--               | 40-later  |
| crossnet56k5_b72e075g3                   | 490    | 4.10   | 27.11/--               | 70-former |
| crossnet65k5_b72e05g2                    | 457    | 3.58   | 27.03/--               | 70-later  |
|                                          |        |        |                        |           |
| crossnet56k5_b64e05_1600_wd2e-5          | 448    | 4.21   | 27.60/--               | 20-former |
| crossnet56k5_b64e05_1600gpu2             | 448    | 4.21   | 27.66/--               | 20-later1 |
| crossnet56k5_b64e05_1600gpu2_24conv1     | 442    | 4.21   | 27.58/--               | 20-later2 |
| crossnet56k5_b64e05_1600                 | 448    | 4.21   | 27.41/27.03            | 21-all    |
| crossnet65k5_b48e075_1600                | 438    | 3.98   | 28.01/--               | 30-former |
| crossnet56k5_b48e075_1600                | 383    | 3.91   | 28.48/28.05            | 30-later  |
| crossnet56ins_b64e05_1600                | 493    | 4.21   | 27.35/--               | 40-former |
| crossnet57k5_b64e05                      | 431    | 3.81   | 27.94/--               | 40-later  |
| crossnet56k5_b64e05_1600_64head          | 474    | 4.22   | 27.14/--               | 70-former |
| crossnet65k5_b60e05_1600                 | 458    | 4.01   | 27.51/--               | 70-later  |
|                                          |        |        |                        |           |
| crossnet57k5_b64e05_24head_type2         | 430    | 3.58   | 28.28/--               | 20-former |
| crossnet57k5_b64e05_24head               | 426    | 3.81   | 28.08/--               | 20-later  |
| crossnet57k5_b64e05g2                    | 315    | 3.09   | 28.49/28.02            | 30-former |
| crossnet57k5_b48e05                      | 259    | 2.79   | 30.13/--               | 30-later  |
| crossnet56k5_b70e04g2_24head             | 309    | 3.00   | 28.39/27.96            | 40-former |
| crossnet56k5_b64e05g2_24head             | 317    | 3.09   | 28.61/--               | 40-later  |
| crossnet56k5_b70e04                      | 434    | 4.09   | 27.43/27.28            | 70-former |
| crossnet56k5_b80e04                      | 548    | 4.76   | 26.70/26.47            | 70-later  |
|                                          |        |        |                        |           |
| crossnet56k5_b70e04g2_24head_relu        | 309    | 3.00   | 28.34/--               | 20-former |
| crossnet56k5_b70e04g2_24head_type3_relu  | 307    | 3.59   | 28.17/27.84            | 20-later  |
| crossnet65k5_b70e04g2_24head_type4       | 348    | 3.81   | 28.02/--               | 21-all    |
| crossnet65k5_b70e04_24head_type3         | 479    | 4.00   | 27.13/--               | 30-former |
| crossnet65k5_b70e04g2_24head_type3       | 350    | 3.22   | 28.20/--               | 30-later  |
| crossnet56k5_b70e04g2_24conv1_relu       | 314    | 3.01   | fail                   | 70-former |
| crossnet56k5_b70e04g2_24conv1_type3_relu | 311    | 3.60   | 28.22/27.89            | 70-later  |
|                                          |        |        |                        |           |
| relu, conv24, 1280tail, type3=1122       | wd3e-5 |        |                        |           |
| crossnet58k5_b70e04g2-1024tail           | 309    | 3.28   | --/--                  | 20-all    |
| crossnet58k5_b70e04g2-bs1024-lr0.4       | 311    | 3.60   | --/--                  | 21-all    |
| crossnet58k3_b70e04g2 (k=3)              | 286    | 3.50   | 28.77/--               | 30-former |
| crossnet58k5_b70e04g2-wd4e-5             | 311    | 3.60   | --/--                  | 30-later  |
| crossnet58k5_b70e04                      | 422    | 4.57   | --/--                  | 40-former |
| crossnet58k5_b70e04g2-1024tail           | 309    | 3.28   | --/--                  | 40-later  |
| crossnet49k5_b80e04g2-1024tail           | 335    | 3.63   | --/--                  | 70-former |
| crossnet49k5_b80e04g2-1024tail-wd4e-5    | 335    | 3.63   | --/--                  | 70-later  |

