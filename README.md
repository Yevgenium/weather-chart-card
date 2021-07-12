![openweathermap-eng](https://user-images.githubusercontent.com/33804747/50649716-d987f880-0fa8-11e9-9608-93aa8b2857f4.png)

## Configuration

Copy `weather-card-chart.js` from this repository into your `config/www` directory first.

Add a reference to the copied file:
```yaml
# Example Lovelace UI config entry
resources:
- type: module
  url: /local/weather-card-chart.js
```
Then you can add the card to the view:
```yaml
# Example Lovelace UI config entry
  - type: 'custom:weather-card-chart'
    title: Weather
    weather: weather.openweathermap
```

#### Configuration variables:

| Name     | Optional | Description                                                                                        |
| -------- | -------- | -------------------------------------------------------------------------------------------------- |
| type     | **No**   | Should be `'custom:weather-card-chart'`                                                            |
| title    | Yes   | Default value: ``. Card title                                                                                         |
| weather  | **No***   | An entity_id with the `weather` domain. Use only one: 'weather' or 'entity' option.                                                             |
| entity  | **No***   | (For backward compatibility with Weather Forecast Card) An entity_id with the `weather` domain. Use only one: 'weather' or 'entity' option.                                                             |
| temp     | Yes      | Entity_id of the temperature sensor. Show temperature value from sensor instead                    |
| temp_apparent | Yes      | Entity_id of the apparent temperature sensor                                                  |
| mode     | Yes      | Default value: `daily`. Set mode to `hourly` to display hours instead weekdays on the chart        |
| wind    | Yes      | Entity_id of the wind sensor. Show wind value from sensor instead                                  |
| wind_unit | Yes      | Default value: `ms`. Set wind_unit to `kmh` to display wind speed in km/h        |
| pressure2mmhg | Yes      | Default value: False. Set pressure2mmhg to True to display pressure in mmHg        |
| chart_only | Yes      | Default value: False. Set chart_only to True to display only temperature chart        |
