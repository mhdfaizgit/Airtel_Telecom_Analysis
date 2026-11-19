# claim : the two group used the same amount of data before the offer 
# H0 : both group have the same true avarage  daily data before May 
# H1 : the two averages deffer


F-test:
F-0.9003
p-3.673 x 10-
Decision: Variances differ.

Z-test:
z - 0.5191
p -0.6037 which >0.05

Decision
Fail to reject H0  

Conclusion

There is Insufficient evidence that the groups differed in their average daily data usage before the effer. The groups are considered balanced on this important pre-offer measure.


# Airtel Telecom – Statistical Validation Report


## 1 Daily data usage in May–June

**Claim:** the offer raised daily data usage
**H0:** both groups have the same true average daily data in May and June
**H1:** group B's average is higher (one-tailed)

F-test: F = 0.6197, p = 8.4 × 10⁻¹¹⁶ → variances differ
Z-test: |z| = 19.45, p ≈ 10⁻⁸⁴ (B is higher than A)

**Decision:** Reject H0
**Conclusion:** There is very strong evidence that the offer raised daily data usage.

## 2 Churn

**Claim:** the offer reduced churn
**H0:** both groups have the same true churn rate
**H1:** group B's churn rate is lower (one-tailed)

| Measure | Group A | Group B | z | p (two-tailed) |
|---|---|---|---|---|
| All churn | 23.53 % (2,587) | 23.98 % (2,639) | 0.7937 | 0.4274 |
| Churn from May on | 8.23 % (905) | 8.31 % (914) | 0.2041 | 0.8382 |

**Decision:** Fail to reject H0
**Conclusion:** There is no evidence that the offer reduced churn. B's churn is actually slightly higher, though not significantly so.

## 3 Recharge revenue from May

**Claim:** the offer raised revenue
**H0:** both groups spent the same on average after May
**H1:** group B's average is higher (one-tailed)

F-test: F = 0.9697, p = 0.1068 → variances similar
t-test: t = −0.5927, p = 0.7233 (> 0.05)

**Decision:** Fail to reject H0
**Conclusion:** There is no evidence that the offer raised recharge revenue.

**Overall result of the offer:** it increased data usage but did not reduce churn or increase revenue.

---

# – What drives churn and usage?

## 4 Prepaid vs Postpaid churn
H0: same churn rate · H1: rates differ
Prepaid 25.90 % (4,441 / 17,149) · Postpaid 16.18 % (785 / 4,851)
z = 14.04, p = 9.3 × 10⁻⁴⁵ → **Reject H0**
Prepaid subscribers churn much more.

## 5 Open ticket vs never complained
H0: same churn rate · H1: rates differ
Open ticket 27.46 % (1,834 / 6,680) · Never complained 20.03 % (1,328 / 6,631)
z = 10.07, p = 7.6 × 10⁻²⁴ → **Reject H0**
Subscribers with an open ticket churn more.

## 6 Tenure: year-0 vs year-3
H0: same churn rate · H1: rates differ
Year-0 28.81 % (1,328 / 4,610) · Year-3 18.73 % (632 / 3,374)
z = 10.33, p = 5.0 × 10⁻²⁵ → **Reject H0**
Newer subscribers churn more.

## 7 Himachal Pradesh vs Punjab
H0: same churn rate · H1: rates differ
Himachal Pradesh 33.44 % (417 / 1,247) · Punjab 13.80 % (77 / 558)
z = 8.65, p = 5.2 × 10⁻¹⁸ → **Reject H0**
(Corrected figure. See Note 1.)

## 8 Smartphone vs Feature phone churn
H0: same churn rate · H1: rates differ
Smartphone 23.76 % · Feature phone 23.74 %
z = 0.0241, p = 0.9807 → **Fail to reject H0**
Device type does not affect churn.

## 9 Region: North vs South
H0: same churn rate · H1: rates differ
North 23.73 % (1,716 / 7,231) · South 21.85 % (1,015 / 4,645)
z = 2.3755, p = 0.0175 → **Reject H0**
(The notebook marked this "not significant". See Note 2.)

## 10 Gender and data usage
H0: same average daily data · H1: averages differ
F-test: F = 0.9315, p = 6.3 × 10⁻¹⁷⁷
Z-test: z = −7.25, p = 4.1 × 10⁻¹³ → **Reject H0** (female lower than male)
Caution: this test used daily rows, not one value per subscriber. See Note 4.

## 11 Device type and data usage
H0: same average daily data · H1: averages differ
F-test: F = 0.0268, p ≈ 0
Z-test: z = −119.24, p ≈ 0 → **Reject H0**
Feature-phone users use far less data than smartphone users.

---

# Summary

| # | Test | Result | Decision |
|---|---|---|---|
| 1.1 | Pre-offer data usage | p = 0.6037 | Balanced |
| 1.2 | Pre-offer revenue | p = 0.1773 | Balanced |
| 1.3 | Smartphone share | p = 0.0109 | Slight imbalance |
| 2.1 | Offer → data usage | p ≈ 10⁻⁸⁴ | **Offer worked** |
| 2.2 | Offer → churn | p = 0.4274 | No effect |
| 2.3 | Offer → revenue | p = 0.7233 | No effect |
| 3.1 | Prepaid vs Postpaid | p ≈ 10⁻⁴⁵ | Prepaid churns more |
| 3.2 | Open ticket vs none | p ≈ 10⁻²⁴ | Open tickets churn more |
| 3.3 | Tenure 0 vs 3 | p ≈ 10⁻²⁵ | New subscribers churn more |
| 3.4 | Himachal vs Punjab | p ≈ 10⁻¹⁸ | Differ |
| 3.5 | Smartphone vs Feature phone churn | p = 0.9807 | No difference |
| 3.6 | North vs South churn | p = 0.0175 | Differ |
| 3.7 | Gender → data | p ≈ 10⁻¹³ | Differ |
| 3.8 | Device → data | p ≈ 0 | Differ |

## Final conclusion

The A/B split was fair on the main pre-offer measures. The offer clearly increased data usage, but it did not reduce churn or raise revenue. Churn is driven mainly by connection type (prepaid), unresolved complaints, short tenure and location, not by device type.

---

# Notes on the notebook (things to fix)

1. **Cell "Himachal vs Punjab"**: the code used 408 / 1,412, which is **Andhra Pradesh**. Himachal Pradesh is 417 / 1,247. The conclusion stays the same, but the numbers change (z = 8.65 instead of 7.01).
2. **North vs South**: the comment says "NOT significant" but p = 0.0175, which is below 0.05. It is significant.
3. **Highest vs lowest circle**: the code compared Maharashtra (470 / 1,428) with Rajasthan (207 / 1,082), and the comment says "NOT significant" even though p = 1.3 × 10⁻¹⁴. Himachal Pradesh (33.4 %) vs Punjab (13.8 %) would be the true highest vs lowest.
4. **Gender test** uses every daily row, so one subscriber counts many times. This inflates the sample and makes p-values too small. Use one average per subscriber, as the device test does.
5. **Payments test (C1)** compares subscriber counts to payment counts (17,149 / 299,670 vs 4,851 / 108,419). That is not a valid comparison of two proportions, so ignore its result.
6. **One-tailed claims** (data, churn, revenue) were run with the default two-tailed option. Use `tail='greater'` or `'less'` with the correct group order. For churn, B lower gives p = 0.786. The decision does not change.
7. **Balance check on stated ARPU, tenure and complaints** only ran the F-test. The averages were never compared.
8. **Smartphone share imbalance** (p = 0.011) was calculated but not commented on.