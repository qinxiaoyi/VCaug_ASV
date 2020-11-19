# VCaug_ASV

The 'trails_key' is the trial file of  "EXPLORING VOICE CONVERSION BASED DATA AUGMENTATION IN TEXT-DEPENDENT SPEAKER VERIFICATION" paper and the ratio of target to nontarget is 1:10.

The final result show in the following table.

|  Model   | Training data  | Spk/Utt Num. | EER\[\%\] | mDCF_{0.1} |
|  ----  | ----  | ----  | ----  | ----  |
| Pre_train model  | AISHELL2+SLR62 + SLR68 | 3472 / 518864 | 6.51 | 0.265 |
| Fine-tune model  | 9utt(baseline) | 340/3060 | 7.63 | 0.331 | 
| -  | + Pitch shift AUG | 1020/9180 | 5.76 | 0.248 |
| -  | + VC AUG_{in}(Mel-to-Mel) | 340/26160 | 6.36 | 0.304 |
| -  | + VC AUG_{in}(PPP-to-Mel) | 340/29089 | 5.16 | 0.249 |
| -  | + VC AUG_{out}(Mel-to-Mel) | 3210/48890 | 6.08 | 0.295 |
| -  | + VC AUG_{in}(Mel-to-Mel) + Pitch shift AUG | 1020/76978 | 5.19 | 0.241 |
| -  | + VC AUG_{in}(PPP-to-Mel) + Pitch shift AUG | 1020/87267 | 0.214 |

