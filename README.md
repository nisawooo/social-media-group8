Source: Kim et al. WSDM 2021
1. Model Description
Two OLS regression approaches were applied to predict post-level engagement rate (likes + comments/followers) across 9,737 Instagram beauty influencer posts.

Models 1–3: Sequential OLS using caption features only, image features only, and all features combined — to compare channel-level explanatory power
Model 4: Tier-stratified OLS re-run separately for micro, mid, and macro influencers

Caption predictors: Sentiment score, caption length, hashtag count, emoji count, CTA flag
Image predictors: Brightness, colorfulness, face presence, edge density

2. Intended Use
Designed to help beauty influencers and social media managers understand which content choices drive engagement, and how optimal strategies shift across audience tiers. Suitable for content planning and benchmarking, not for influencer contract decisions or campaign budget allocation.

3. Fairness Considerations
The dataset covers Instagram only; findings may not generalise to TikTok or YouTube
Macro-tier subsample is smaller (n=1,854) and may produce less stable estimates
Engagement rate is partly shaped by Instagram's algorithm, which the model cannot account for


4. Limitations
R² values are low (0.018-0.033), content features explain only a small share of engagement variance; posting time, trends, and algorithm state are not captured
Correlation only face presence predicting higher engagement does not mean adding a face will causally increase engagement
Cross-sectional design; it does not capture how strategies evolve over time
