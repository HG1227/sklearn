# feature_selection.SelectKBest用法

根据评分，选取的评分较高的 k 个特征。



```python
class sklearn.feature_selection.SelectKBest(score_func=<function f_classif>, 
                                            k=10
                                           )
```

**Parameters**

**`score_func`**

**callable**

函数接受两个数组X和y，并返回一对数组（分数，pvalue）或带分数的单个数组。

**`k`**

**int or “all”, optional, default=10**

Number of top features to select

<br>

**Attributes**

**`scores_`**

array-like of shape (n_features,)

Scores of features.

**`pvalues_`**

array-like of shape (n_features,)

p-values of feature scores, None if `score_func` returned only scores.



**Methods**

| [`fit`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.fit)(self, X, y) | Run score function on (X, y) and get the appropriate features. |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [`fit_transform`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.fit_transform)(self, X[, y]) | Fit to data, then transform it.                              |
| [`get_params`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.get_params)(self[, deep]) | Get parameters for this estimator.                           |
| [`get_support`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.get_support)(self[, indices]) | Get a mask, or integer index, of the features selected       |
| [`inverse_transform`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.inverse_transform)(self, X) | Reverse the transformation operation                         |
| [`set_params`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.set_params)(self, \*\*params) | Set the parameters of this estimator.                        |
| [`transform`](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest.transform)(self, X) | Reduce X to the selected features.                           |

