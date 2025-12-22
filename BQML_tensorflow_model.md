# BigQuery ML: TensorFlow SavedModel Import

BigQuery ML lets you import a pre-trained TensorFlow SavedModel directly from Cloud Storage and run predictions in SQL. This is the simplest path for a SQL analyst: no serving infrastructure, no endpoints—just `CREATE MODEL ... MODEL_TYPE='TENSORFLOW'` pointing to your `gs://` model and then `ML.PREDICT`.

### Foundational concept:
BigQuery ML (BQML) enables analysts to train and use models with SQL. For supported external frameworks like TensorFlow, BQML supports importing a SavedModel from Cloud Storage and running predictions via standard SQL.

### How it applies here:
1. Your TensorFlow model is already in Cloud Storage as a SavedModel.
2. In BigQuery, run:

```sql
CREATE OR REPLACE MODEL `dataset.segmenter`
OPTIONS (
  MODEL_TYPE = 'TENSORFLOW',
  MODEL_PATH = 'gs://your-bucket/path/to/exported_saved_model'
);

```

3. Use it with SQL:

```sql
SELECT *
FROM ML.PREDICT(
  MODEL `dataset.segmenter`,
  TABLE `dataset.customer_features`
);

```

---

This avoids provisioning/operating endpoints, IAM wiring for online prediction, or writing glue code—fastest and least complex for a SQL-only workflow.

* Simplicity: All-SQL workflow; no serving stack.
* Efficiency: Pushes scoring to BigQuery’s distributed engine on your data in place.
* Governance & cost: No extra online prediction infra; benefits from BigQuery’s security, quotas, and billing model.

* 
