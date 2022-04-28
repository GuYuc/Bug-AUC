# Bug-AUC

System, programs or code toolkits would report bug/error information when something goes wrong. Generally, a bug report should be regarded as a bug, and actions must be taken to avoid it. But as program grows more and more complicated, one may find out that some bug/error information would not affect system correctness. For example, one day you found a goddamn error message in your program log, which happens every day and every hour, and you try to figure out its causes, but finally another colleague tells you just ignore this error message because it is not a real bug and it do no harm to your system. On the other hand, your program may go wrong without any error or bug message, which also could happens every day and every hour, finally it takes you lots of expensive efforts to corretify your program. 


| | Bug Report | No Bug Report |
| ---- | ---- | ---- |
| Real Bug | True Positive (TP) | **False Negative (FN)** |
| No Bug | False Positive (FP) | True Negative (TN) |


As is mentioned above, some bug reports does not mean actual bugs, so these can be regarded as False Positives (FP) Bugs. Conversely, some real bugs are not reported, which are considered as False Negatives (FN). FN bugs are more harmful than FP bugs. With True Positive (TP) and True Negative (TN) definition, precision, recall and f1-score can be calculated, just like what we do in assessing binary classification models. Furthermore, If we've got a model in every bug report that tells us the bug probability in such case, an AUC score can be evaluated, which is called Bug-AUC.
