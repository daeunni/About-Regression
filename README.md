## 회귀 분석 팀플(2020.6월)
https://www.kaggle.com/danevans/world-bank-wdi-212-health-systems/kernels
1. 요 캐글 데이터로,,, 외부 데이터를 합친 뒤 새로운 데이터 셋을 만들었다!
2. 전처리에 주안점을 둔 것
- 완전 많은 결측치 처리
- 다중공선성 해결
- 유의미한 피쳐 생성(2016년 의료데이터 넘나 무의미한것)

3. 회귀모델 적합 시 주안점을 둔 것
- 잔차가정을 만족하는가? (선형성)
- 등분상성을 만족하는가?
- **다중공선성**

4. 결과
- c_lm_log_del2 <- lm(log(ConfirmedCases)~days_from_case_100+days_from_first_death+log(pop)+Health_exp_per_capita_USD_2016+per_capita_exp_PPP_2016)
summary(c_lm_log_del2);plot(c_lm_log_del2) 로 적합한 결과
 
R스퀘어 : 0.779
F : 103.8
잔차 : 굿굿
