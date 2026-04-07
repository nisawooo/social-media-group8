Source: Kim et al. WSDM 2021
1. Model Description
Two OLS regression approaches were applied to predict post-level engagement rate (likes + comments/followers) across 9,737 Instagram beauty influencer posts.

Models 1–3: Sequential OLS using caption features only, image features only, and all features combined - to compare channel-level explanatory power
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

5. References
Belanche, D., Casaló, L.V., Flavián, M. and Ibáñez-Sánchez, S. (2021) 'Building influencers' credibility on Instagram: Effects on followers' attitudes and behavioral responses toward the influencer', Journal of Retailing and Consumer Services, 61, p.102585. doi:10.1016/j.jretconser.2021.102585.
Boerman, S.C. (2020) 'The effects of the standardized Instagram disclosure for micro- and meso-influencers', Computers in Human Behavior, 103, pp.199–207. doi:10.1016/j.chb.2019.09.015.
Cheung, M.L., Leung, W.K., Aw, E.C.X. and Koay, K.Y. (2022) '"I follow what you post!": the role of social media influencers' content characteristics in consumers' online brand-related activities (COBRAs)', Journal of Retailing and Consumer Services, 66, p.102940. doi:10.1016/j.jretconser.2022.102940.
De Veirman, M., Cauberghe, V. and Hudders, L. (2017) 'Marketing through Instagram influencers: the impact of number of followers and product divergence on brand attitude', International Journal of Advertising, 36(5), pp.798-828. doi:10.1080/02650487.2017.1348035.
Erz, A., Marder, B. and Osadchaya, E. (2018) 'Hashtags: Motivational drivers, their use, and differences between influencers and followers', Computers in Human Behavior, 89, pp.48–60. doi:10.1016/j.chb.2018.07.030.
Gelli, F., Uricchio, T., Bertini, M., Del Bimbo, A. and Chang, S.-F. (2015) 'Image popularity prediction in social media using sentiment and context features', in Proceedings of the 23rd ACM International Conference on Multimedia. New York: ACM, pp.907–910. doi:10.1145/2733373.2806361.
Hasler, D. and Suesstrunk, S.E. (2003) 'Measuring colorfulness in natural images', in Human Vision and Electronic Imaging VIII, Proceedings of SPIE, 5007, pp.87–95. doi:10.1117/12.477378.
Hutchinson, A. (2022) 'New report highlights that Instagram hashtags don't significantly increase post engagement', Social Media Today, 18 April. Available at: https://www.socialmediatoday.com/news/new-report-highlights-that-instagram-hashtags-dont-significantly-increase/622260/ (Accessed: 7 April 2026).
Hutto, C. and Gilbert, E. (2014) 'VADER: A parsimonious rule-based model for sentiment analysis of social media text', in Proceedings of the Eighth International Conference on Weblogs and Social Media (ICWSM-14). Palo Alto: AAAI Press, pp.216–225.
Instagram [@creators] (2025) 'New hashtag guidance: Starting today, Instagram will allow up to 5 hashtags in a reel or post' [Threads post], 18 December. Available at: https://www.threads.com/@creators/post/DSalXGPCWM4 (Accessed: 7 April 2026).
Kim, S., Jiang, J.-Y., Nakada, M., Han, J. and Wang, W. (2020) 'Multimodal post attentive profiling for influencer marketing', in Proceedings of The Web Conference 2020 (WWW '20). New York: ACM, pp.2878–2884. doi:10.1145/3366423.3380052.
Tafesse, W. and Wood, B.P. (2021) 'Followers' engagement with Instagram influencers: The role of influencers' content and engagement strategy', Journal of Retailing and Consumer Services, 58, p.102303. doi:10.1016/j.jretconser.2020.102303.

6. Benchmark different techniques
Model                        |    Why we did not use it
                             |
Logistic regression          |    Our outcome (engagement rate) is continuous, not binary
                             | 
Random forest/ XBoost        |    Black box — cannot extract directional coefficients for advice
                             |
LASSO / Ridge                |    Useful for high-dimensional feature selection — we only have 9 features, no  
                             |    regularisation needed
                             |
Fixed effects panel          |    Would require multiple posts per influencer over time — our data is cross-
                             |    sectional
                             |
Poisson / negative binomial  |    Appropriate for count outcomes — engagement rate is continuous
                             |
Neural network               |    Prediction tool, not explanation tool - R° of 0.024 would not justify the 
                             |    complexity cost









