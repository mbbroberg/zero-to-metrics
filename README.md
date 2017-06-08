# zero-to-metrics [Alpha]

I'd like a simple dashboard of metrics over time without being deep on any of the pieces to get there. 

## Disclaimer

On their own they are vanity metrics, but when you look at trends you can find patterns worth sharing. Whatever you do, please do not use this to report on meaningless statistics like number of commits on the project. 

## How it got it to work 

Running on macOS, I did the following: 

* `brew install elasticsearch` and ran with the default settings
* `brew install kibana` and ran with the default settings
* `brew install python3` which includes `pip3`
* `pip3 install grimoire_elk` which includes `p2o.py`
* `which p2o.py` to ensure it is in the path, otherwise find it
* Update `PATH_TO_P2O` and the array of repositories to check in `runner.sh`
* Run it while ElasticSearch is running and you should get data in there!
* Load Grimoire's [Git Dashboard][1] to have a handy default
* Explore the data in Discover tab of Kibana at http://localhost:5601/app/kibana#/discover

![Kibana Discovery](https://user-images.githubusercontent.com/1744971/26947182-a0b24154-4c46-11e7-9c6a-d25c0368bfbd.gif)

[1]: https://raw.githubusercontent.com/jgbarah/GrimoireLab-training/master/grimoireelk/dashboards/git-dashboard.json