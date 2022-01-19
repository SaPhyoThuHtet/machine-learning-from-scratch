**3.1 Interpretability**
If a machine learning model performs well, why do we not just trust the model and ignore why it made a certain decision? 
“The problem is that a single metric, such as classification accuracy, is an incomplete description of most real-world tasks.” 
(Doshi-Velez and Kim 2017 6)

**3.2 Taxonomy of Interpretability Methods**

**Intrinsic or post hoc?**
Intrinsic interpretability refers to machine learning models that are considered interpretable due to their simple structure, such as short decision trees or sparse linear models.

Post hoc interpretability refers to the application of interpretation methods after model training. Permutation feature importance is, for example, a post hoc interpretation method.

Post hoc methods can also be applied to intrinsically interpretable models. For example, permutation feature importance can be computed for decision trees.


**Model-specific or model-agnostic?**

Model-specific interpretation tools are limited to specific model classes. The interpretation of regression weights in a linear model is a model-specific interpretation, since – by definition – the interpretation of intrinsically interpretable models is always model-specific. Tools that only work for the interpretation of e.g. neural networks are model-specific. 

Model-agnostic tools can be used on any machine learning model and are applied after the model has been trained (post hoc). These agnostic methods usually work by analyzing feature input and output pairs. By definition, these methods cannot have access to model internals such as weights or structural information.

**Local or global?** 
Does the interpretation method explain an individual prediction or the entire model behavior? Or is the scope somewhere in between? 





