# Data Source Options for Real-Time Lakehouse Project

## Option A: Real Data (Crawled from Internet)
- **Traffic Data:**
  - Example: [NYC MTA Real-Time Data](http://datamine.mta.info/list-of-feeds)
  - Example: [Transport for London Unified API](https://api.tfl.gov.uk/)
- **Air Quality Data:**
  - Example: [OpenAQ API](https://docs.openaq.org/)
  - Example: [OpenWeatherMap API](https://openweathermap.org/api)
- **Approach:**
  - Write Python scripts to fetch/crawl data from these APIs at regular intervals.
  - Push the fetched data to Kafka topics (`traffic_stream`, `air_quality_stream`).

## Option B: Fake Data (Generated with Python Library)
- **Traffic Data:**
  - Use Python libraries like `faker`, `numpy`, or custom scripts to simulate vehicle counts, speed, congestion, etc.
- **Air Quality Data:**
  - Use `faker`, `random`, or `numpy` to generate PM2.5, PM10, CO, NO2, O3, temperature, humidity, etc.
- **Approach:**
  - Write Python scripts to generate fake data at desired frequency.
  - Push the generated data to Kafka topics (`traffic_stream`, `air_quality_stream`). 