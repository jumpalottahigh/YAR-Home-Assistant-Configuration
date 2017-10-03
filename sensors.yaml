# Weather sensor
- platform: yr
  monitored_conditions:
  - temperature
  - symbol
  - humidity

# Darksky weather sensor
- platform: darksky
  api_key: !secret darksky_key
  monitored_conditions:
    - precip_probability
    - temperature
    - precip_intensity

# Time and date sensor
- platform: time_date
  display_options:
    - 'date'
    - 'time'

# Net status
- platform: speedtest
  monitored_conditions:
    - ping
    - download
    - upload

# Backyard soil sensors
- platform: mqtt
  state_topic: "home/backyard/soil"
  name: "Soil Moisture Tomatoes"
  unit_of_measurement: "%"
  value_template: '{{ value_json.moisture1 | round(2) }}'

- platform: mqtt
  state_topic: "home/backyard/soil"
  name: "Soil Moisture Potatoes"
  unit_of_measurement: "%"
  value_template: '{{ value_json.moisture2 | round(2) }}'

- platform: mqtt
  state_topic: "home/backyard/soil"
  name: "Soil Moisture Onions"
  unit_of_measurement: "%"
  value_template: '{{ value_json.moisture3 | round(2) }}'

# Xiaomi Mi Flora sensor
# - platform: miflora
#   mac: 'C4:7C:8D:64:31:1F'

### ESP8266 Multisensors - Node 1
- platform: mqtt
  state_topic: "home/sensornode1"
  name: "SN1 Humidity"
  unit_of_measurement: "%"
  value_template: '{{ value_json.humidity | round(1) }}'

- platform: mqtt
  state_topic: "home/sensornode1"
  name: "SN1 LDR"
  ##This sensor is not calibrated to actual LUX. Rather, this a map of the input voltage ranging from 0 - 1023.
  unit_of_measurement: "LUX"
  value_template: '{{ value_json.ldr }}'

- platform: mqtt
  state_topic: "home/sensornode1"
  name: "SN1 PIR"
  value_template: '{{ value_json.motion }}'

- platform: mqtt
  state_topic: "home/sensornode1"
  name: "SN1 Temperature"
  unit_of_measurement: "°C"
  value_template: '{{ value_json.temperature | round(1) }}'

### ESP8266 Multisensors - Node 2
- platform: mqtt
  state_topic: "home/sensornode2"
  name: "SN2 Humidity"
  unit_of_measurement: "%"
  value_template: '{{ value_json.humidity | round(1) }}'

- platform: mqtt
  state_topic: "home/sensornode2"
  name: "SN2 LDR"
  ##This sensor is not calibrated to actual LUX. Rather, this a map of the input voltage ranging from 0 - 1023.
  unit_of_measurement: "LUX"
  value_template: '{{ value_json.ldr }}'

- platform: mqtt
  state_topic: "home/sensornode2"
  name: "SN2 PIR"
  value_template: '{{ value_json.motion }}'

- platform: mqtt
  state_topic: "home/sensornode2"
  name: "SN2 Temperature"
  unit_of_measurement: "°C"
  value_template: '{{ value_json.temperature | round(1) }}'