**3.1 Interpretability**
If a machine learning model performs well, why do we not just trust the model and ignore why it made a certain decision? 
“The problem is that a single metric, such as classification accuracy, is an incomplete description of most real-world tasks.” 
(Doshi-Velez and Kim 2017 6)

**3.2 Taxonomy of Interpretability Methods**
**Intrinsic or post hoc?**
Intrinsic interpretability refers to machine learning models that are considered interpretable due to their simple structure, such as short decision trees or sparse linear models.
Intrinsic ဆိုတာ ရိုးရှင်းတဲ့ decision tree တို့ linear model လိုမျိုးကို​ပြောတာ။

Post hoc interpretability refers to the application of interpretation methods after model training. Permutation feature importance is, for example, a post hoc interpretation method.
Model train ပြီးမှ သုံးတဲ့ interpretation methods ​တွေကို ဆိုလိုတာ။ ဥပမာ- permutation feature importance [8.5 link ချိတ်ရန်]

Post hoc methods can also be applied to intrinsically interpretable models. For example, permutation feature importance can be computed for decision trees.

**Result of the interpretation method**
 The various interpretation methods can be roughly differentiated according to their results.

**Feature Summary Statistics**: 
Many interpretation methods provide summary statistics for each feature.
Some methods return a single number per feature, such as feature importance, or a more complex result, such as the pairwise feature interaction strengths, which consist of a number for each feature pair.
ဒီမှာကကျ feature importance လိုမျိုး pairwise feature interaction strengths လိုမျိုးကို ပြ​ပေးတယ်။

**Feature summary visualization:** 
Most of the feature summary statistics can also be visualized. 
Some feature summaries are actually only meaningful if they are visualized and a table would be a wrong choice.
တခါတ​လေကျ feature summaries ​တွေက table အစား visualize လုပ်မှ ပို meaningful ဖြစ်တာမျိုးရှိတယ်။
The partial dependence of a feature is such a case. 
Partial dependence plots are curves that show a feature and the average predicted outcome. 
The best way to present partial dependences is to actually draw the curve instead of printing the coordinates.

**
Model internals (e.g. learned weights):**
Linear models လိုမျိုးဟာ​​တွေရဲ့ weights က models internals ​​ကော frature summary statistics အတွက်​ကော တူတူပဲဖြစ်​နေလို့။
The interpretation of intrinsically interpretable models falls into this category.
Examples are the weights in linear models or the learned tree structure (the features and thresholds used for the splits) of decision trees. 
The lines are blurred between model internals and feature summary statistic in, for example, linear models, because the weights are both model internals and summary statistics for the features at the same time. 

​နောက်တစ်ခုက​တော့ CNN ရဲ့feature detectors ​တွေကို ​visualize လုပ်တာမျိုးကလည်း model internals ပဲ။
Another method that outputs model internals is the visualization of feature detectors learned in convolutional neural networks. 

Model internals ​တွေက model specific ဖြစ်တယ်။
Interpretability methods that output model internals are by definition model-specific (see next criterion).

**Model-specific or model-agnostic?**

Model-specific interpretation tools are limited to specific model classes. The interpretation of regression weights in a linear model is a model-specific interpretation, since – by definition – the interpretation of intrinsically interpretable models is always model-specific. Tools that only work for the interpretation of e.g. neural networks are model-specific. 

Model-agnostic tools can be used on any machine learning model and are applied after the model has been trained (post hoc). These agnostic methods usually work by analyzing feature input and output pairs. By definition, these methods cannot have access to model internals such as weights or structural information.

**Local or global?** 
Does the interpretation method explain an individual prediction or the entire model behavior? Or is the scope somewhere in between? 





