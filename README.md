# Smart City Hackathon

This map was built during the [Smart City Hackathon](http://smrtsandbox.com/challenge/smart-city-hackathon-presented-by-smart-columbus/) and is powered by [Leaflet](http://leafletjs.com/).

## Downloading the Data

You'll need an API Key from the Smart Columbus Sandbox.

```bash
for ((i=0; i<7; i++)); do
  curl \
    --header 'Content-Type: application/json' \
    --data "{ \"weekday\": $i, \"apiKey\": \"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\" }" \
    -X POST \
    'http://smrtsandbox.com:8080/rest/columbus-driving-data/get' > columbus-driving-data-$i.json
done
```

## Columbus Map

![map](https://github.com/dan-manges/smart-city-hackathon-columbus-map/raw/master/columbus-map.png)
