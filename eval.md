### Mean Reciprocal Rank (MRR)

```python
def mean_reciprocal_rank(y_true, y_pred):
    """
    Calculate Mean Reciprocal Rank (MRR)
    
    y_true: List of lists containing the true relevant items.
    y_pred: List of lists containing the predicted items ranked.
    
    Returns:
    MRR score.
    """
    MRR = 0
    for true, pred in zip(y_true, y_pred):
        for rank, item in enumerate(pred, start=1):
            if item in true:
                MRR += 1 / rank
                break
    return MRR / len(y_true)
```

### Hits @ K
```python
def hits_at_k(y_true, y_pred, k):
    """
    Calculate Hits@k for a single query.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    k: The number of top results to consider.
    
    Returns:
    Hits@k score (1 if at least one relevant item is in top k, else 0).
    """
    pred_at_k = y_pred[:k]
    if set(pred_at_k) & set(y_true):
        return 1
    else:
        return 0


def mean_hits_at_k(y_true, y_pred, k):
    """
    Calculate Mean Hits@k across all queries.
    
    y_true: List of lists containing the true relevant items.
    y_pred: List of lists containing the predicted items ranked.
    k: The number of top results to consider.
    
    Returns:
    Mean Hits@k score.
    """
    hits_scores = [hits_at_k(true, pred, k) for true, pred in zip(y_true, y_pred)]
    return sum(hits_scores) / len(hits_scores)
```

### Mean Average Precision (mAP)

```python
def average_precision(y_true, y_pred):
    """
    Calculate Average Precision for a single query.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    
    Returns:
    Average Precision score.
    """
    hits = 0
    sum_precisions = 0
    for rank, item in enumerate(y_pred, start=1):
        if item in y_true:
            hits += 1
            sum_precisions += hits / rank
    if hits == 0:
        return 0
    return sum_precisions / len(y_true)


def mean_average_precision(y_true, y_pred):
    """
    Calculate Mean Average Precision (MAP) over all queries.
    
    y_true: List of lists containing the true relevant items.
    y_pred: List of lists containing the predicted items ranked.
    
    Returns:
    MAP score.
    """
    return sum(average_precision(t, p) for t, p in zip(y_true, y_pred)) / len(y_true)
```

### Normalized Discounted Cumulative Gain (NDCG @ K)

```python
import numpy as np

def dcg_at_k(y_true, y_pred, k):
    """
    Calculate Discounted Cumulative Gain (DCG) at K.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    k: The rank position till where DCG is calculated.
    
    Returns:
    DCG score.
    """
    dcg = 0
    for rank, item in enumerate(y_pred[:k], start=1):
        if item in y_true:
            dcg += 1 / np.log2(rank + 1)
    return dcg


def ndcg_at_k(y_true, y_pred, k):
    """
    Calculate Normalized Discounted Cumulative Gain (nDCG) at K.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    k: The rank position till where nDCG is calculated.
    
    Returns:
    nDCG score.
    """
    dcg = dcg_at_k(y_true, y_pred, k)
    ideal_dcg = dcg_at_k(y_true, y_true, k)
    return dcg / ideal_dcg if ideal_dcg > 0 else 0


def mean_ndcg_at_k(y_true, y_pred, k):
    """
    Calculate Mean nDCG at K over all queries.
    
    y_true: List of lists containing the true relevant items.
    y_pred: List of lists containing the predicted items ranked.
    k: The rank position till where nDCG is calculated.
    
    Returns:
    Mean nDCG score.
    """
    return sum(ndcg_at_k(t, p, k) for t, p in zip(y_true, y_pred)) / len(y_true)
```

### Precision @ K

```python
def precision_at_k(y_true, y_pred, k):
    """
    Calculate Precision@k.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    k: The number of top results to consider.
    
    Returns:
    Precision@k score.
    """
    pred_at_k = y_pred[:k]
    relevant_at_k = set(pred_at_k) & set(y_true)
    return len(relevant_at_k) / k

```

### Recall @ K

```python
def recall_at_k(y_true, y_pred, k):
    """
    Calculate Recall@k.
    
    y_true: List of true relevant items.
    y_pred: List of predicted items ranked.
    k: The number of top results to consider.
    
    Returns:
    Recall@k score.
    """
    pred_at_k = y_pred[:k]
    relevant_at_k = set(pred_at_k) & set(y_true)
    return len(relevant_at_k) / len(y_true)
```

### F1 Score (QA)

```python
def f1_score(y_true, y_pred):
    """
    Calculate F1 score.
    
    y_true: List of ground truth answers.
    y_pred: List of predicted answers.
    
    Returns:
    Average F1 score over all predictions.
    """
    def _f1_single(true, pred):
        true_tokens = true.split()
        pred_tokens = pred.split()

        common_tokens = set(true_tokens) & set(pred_tokens)
        if len(common_tokens) == 0:
            return 0

        precision = len(common_tokens) / len(pred_tokens)
        recall = len(common_tokens) / len(true_tokens)
        f1 = 2 * (precision * recall) / (precision + recall)
        return f1

    f1_scores = [_f1_single(true, pred) for true, pred in zip(y_true, y_pred)]
    return sum(f1_scores) / len(f1_scores)
```