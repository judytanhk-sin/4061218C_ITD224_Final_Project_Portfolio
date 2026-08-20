# AI Ethics Assessment

## HDB Resale Price Prediction Project

This assessment considers the ethical risks associated with collecting, analysing and modelling HDB resale transaction data. The objective is to ensure that the model is used responsibly, transparently and fairly.

---

## 1. Data Privacy

The dataset contains publicly available HDB resale transaction information. Personal identifiers such as buyers' names, identification numbers, telephone numbers and email addresses were not collected or used.

**Risk:** Combining transaction data with other sources could unintentionally reveal information about individuals or households.

**Mitigation:**

- Use only information necessary for resale-price prediction.
- Exclude personally identifiable information.
- Store the dataset securely.
- Restrict access to authorised users.
- Follow applicable data-protection requirements.

---

## 2. Fairness and Bias

The model learns from historical resale transactions. Historical prices may reflect differences between towns, flat types, lease periods and other market conditions.

**Risk:** The model may produce less accurate predictions for locations or flat categories that have fewer transactions.

**Mitigation:**

- Evaluate model performance across towns and flat types.
- Compare MAE and RMSE for different property segments.
- Investigate segments with unusually high prediction errors.
- Retrain the model using representative and updated data.
- Avoid using sensitive personal characteristics.

---

## 3. Transparency and Explainability

Users should understand the main factors affecting the predicted resale price.

**Mitigation:**

- Report the model type and selected features.
- Present feature importance results.
- Explain the effects of floor area, town, remaining lease, storey and resale year.
- Clearly disclose the model's assumptions and limitations.
- Present predictions as estimates rather than guaranteed market values.

---

## 4. Accuracy and Reliability

Property-market conditions can change over time. A model trained using historical transactions may become less accurate when market conditions change.

**Mitigation:**

- Use chronological training and testing.
- Evaluate the model using MAE, RMSE and R².
- Monitor prediction errors after deployment.
- Retrain the model regularly with recent transactions.
- Conduct data-quality checks before generating predictions.

---

## 5. Accountability

The project team remains responsible for how the model is designed, evaluated and communicated.

**Mitigation:**

- Document data-cleaning and modelling decisions.
- Maintain model and dataset version records.
- Review abnormal or high-impact predictions.
- Provide a process for reporting and correcting errors.
- Assign responsibility for model monitoring and maintenance.

---

## 6. Human Oversight

The prediction model should support decision-making and should not replace professional property valuation or financial advice.

Final pricing decisions should also consider:

- Current market conditions
- Property condition and renovation
- Exact location and nearby amenities
- Recent comparable transactions
- Professional valuation
- Buyer and seller circumstances

---

## 7. Security and Responsible Use

The model, dataset and generated predictions should be protected against unauthorised access or misuse.

**Mitigation:**

- Control access to project files.
- Avoid publishing sensitive information.
- Validate input data before prediction.
- Keep software dependencies updated.
- Prevent the model from being presented as an official valuation service.

---

## Ethical Risk Summary

| Ethical Area | Potential Risk | Mitigation |
|---|---|---|
| Privacy | Identification of individuals or households | Exclude personal identifiers and use only necessary data |
| Fairness | Unequal accuracy across towns or flat types | Conduct segment-level performance evaluation |
| Transparency | Users may not understand predictions | Provide feature importance, assumptions and limitations |
| Reliability | Model performance may decline over time | Monitor errors and retrain with recent data |
| Accountability | Unclear responsibility for incorrect predictions | Maintain documentation and assign model ownership |
| Human oversight | Excessive reliance on automated predictions | Use the model as decision support only |
| Security | Unauthorised access or misuse | Apply access control and secure data handling |

---

## Conclusion

The project applies responsible AI principles by protecting privacy, evaluating potential bias, explaining model behaviour and maintaining human oversight. The resale-price prediction should be treated as a decision-support estimate rather than a guaranteed valuation. Continuous monitoring and periodic retraining are required to maintain fairness, accuracy and reliability
