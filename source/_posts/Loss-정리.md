---
title: Loss 정리
date: 2019-10-07 15:13:51
tags: mse, kld, categorical cross entropy
---
# 평균 제곱 오차(Mean squared error, mse)
- <b>function def.</b>
<div class="colorscripter-code" style="color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#fafafa;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #e5e5e5"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#666;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#010101;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#ff3399">def</span>&nbsp;mean_squared_error(y_true,&nbsp;y_pred):</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff3399">return</span>&nbsp;((y_pred&nbsp;<span style="color:#0086b3"></span><span style="color:#ff3399">-</span>&nbsp;y_true)<span style="color:#0086b3"></span><span style="color:#ff3399">*</span><span style="color:#0086b3"></span><span style="color:#ff3399">*</span><span style="color:#308ce5">2</span>).mean(axis<span style="color:#0086b3"></span><span style="color:#ff3399">=</span>None)</div></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#e5e5e5;color:white;border-radius:10px;padding:1px">cs</span></a></td></tr></table></div>
<br>
- 실제 값, 예측 값 사이의 차이를 최소화

# 쿨백 라이블러 발산(Kullback-Leibler divergnece, KLD)
- 두 확률 분포의 차이를 계산. 정보 엔트로피 차이를 계산. 
  학습 데이터와 모델이 예측한 데이터의 분포 간에 차이 계산.

# categorical cross entropy