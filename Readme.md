# Install #
1. ```bash
    docker-compose up -d
    ```
2. Go to [127.0.0.1:8080](127.0.0.1:8080)
3. Login params ```    "username": "freqtrader",
   "password": "password"```

# Links #
Your best friend is [documentation](https://www.freqtrade.io/en/stable/)

Free [strategies](https://github.com/freqtrade/freqtrade-strategies/tree/master/user_data/strategies) repo

Youtube:
   Playlist with few tutorials [OMG The Cloud](https://www.youtube.com/watch?v=DjtldeE8jNQ&list=PL-qdqFfJP2m8KVvH6fTDd04ZKluskY6qS)
# Most used commands #
### Show logs ###
```bash
docker logs freqtrade -f
```
### Download data for backtesting, need to be done first ###
```bash
docker-compose run --rm freqtrade download-data --timeframe 5m --config user_data/bt_conf.json
```
### Backtesting strategy  ###
```bash
docker-compose run --rm freqtrade backtesting --timeframe 5m --config user_data/bt_conf.json -s SmoothScalp
```
### Backtesting strategy list ###
```bash
docker-compose run --rm freqtrade backtesting --strategy-list ADXMomentum ClucMay72018 MACDStrategy_crossed Simple AdxSmas CMCWinner MACDStrategy ASDTSRockwellTrading CofiBitStrategy SmoothScalp AverageStrategy CombinedBinHAndCluc DoesNothingStrategy Quickie BbandRsi EMASkipPump ReinforcedQuickie ReinforcedSmoothScalp CCIStrategy Low_BB Scalp --timeframe 4h --config user_data/bt_conf.json
```


## TODO ##
- [ ] Makefile
- [ ] Deploy to cloud
- [ ] Checkout new version with instance integration

[comment]: <> (### DONE ###)

[comment]: <> (- [x] text)