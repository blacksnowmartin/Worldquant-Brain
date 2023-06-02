BASIC OPERATORS

group_neutralize(volume/(ts_sum(volume,60)/60,sector) 
dec 6 trun 0.1

ts_step(20)*volume/(ts_sum(volume,60)/60)


-(today's price- yesterday's price)

Rank( - (close - (ts_product(close,5))^(0.2))
Top 3000
0.1 Trunc Dec 6 D1

ALTERNATIVELY

rank(- signedpower (close-sum(close,5)/5,2))

ts-corr(rank(close)
rank(volume/adv20),5)


ts_sum(-returns.5)
ts_decay_linear
(volume/adv20,5,dense=false)

SCALE OPERATOR
A =ts_sum(-returns.5)
B =ts_decay_linear(volume/adv20,5);
rank(scale(A, scale=1, longscale=1, shortscale=1)
+scale(B, scale=1, longscale=1, shortscale=1))

NEUTRALIZATION
rank(group_mean(ts_delta(close,5),
Delay 0
1,subindustry)-ts_delta(close,5))



TIME OPERATORS
(rank(eps/last_diff_value(eps,5))>0.7
|| volume>ts_delay(volume,1))?
rank(-ts_delta(close,5)):-1

triggerTradeexp = (ts_arg_max(volume,5) <1)
&& (volume>=ts_sum(volume,5)/5);
triggerExitexp = -1;
alphaexp = -rank(ts_delta(close,2));
trade_when(triggerTradeexp,alphaexp,triggerExitexp)

Log(pasteurize(vwap/close))

rank(ts_covariance(ts_std_dev
(-returns,22),(vwap_close),22))


A=ts_regression(close,close,20 lag=1, rettype=3);
B=ts_sum(ts_delay(close,1),2)/2;
C=(A-B)/close;
D=1-rank(volume/ts_sum(volume,30)/30;
-ts_rank(C,60)*D

-(ts_sum(close-min(low,ts_delay(close,1)),5)/
ts_sum(max(high,ts_delay(close,1))-low,5))
Use D0 

-rank((close-ts_max(high,5))/
(ts_max(high,5))-ts_min(low,5)) 
