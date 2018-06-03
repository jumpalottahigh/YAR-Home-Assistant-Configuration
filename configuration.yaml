homeassistant:
  # Name of the location where Home Assistant is running
  name: Yanev Residence
  # Location required to calculate the time the sun rises and sets
  latitude: !secret home_latitude
  longitude: !secret home_longitude
  # Impacts weather/sunrise data (altitude above sea level in meters)
  elevation: !secret home_elevation
  # metric for Metric, imperial for Imperial
  unit_system: metric
  # Pick yours from here: http://en.wikipedia.org/wiki/List_of_tz_database_time_zones
  time_zone: !secret time_zone
  customize: !include customize.yaml

# Show links to resources in log and frontend
#introduction:

# Enables the frontend
frontend:
  # Add themes
  themes: !include themes.yaml
  # Enable ES6 features
  javascript_version: latest

# Add Alexa integration
emulated_hue:
  host_ip: !secret emulated_hue_ip
  listen_port: 80
  # Google Home set up
  # type: google_home

http:
  base_url: !secret ha_base_url
  # ssl_certificate: /ssl/fullchain.pem
  # ssl_key: /ssl/privkey.pem
  api_password: !secret ha_api_password

map:

# Tradfri
# tradfri:
#   host: !secret tradfri_ip
#   api_key: !secret tradfri_api
#   allow_tradfri_groups: false

# Checks for available updates
updater:

# Discover some devices automatically
discovery:

# Allows you to issue voice commands from the frontend in enabled browsers
conversation:

# Enables support for tracking state changes over time.
history:

# View all events in a logbook
logbook:

# Shopping list
# shopping_list:

# Track the sun
sun:

# Config panel enabler
config:

# Home Assistant Cloud
# cloud:

# Text to speech
tts:
  - platform: google
    language: 'en-us'

# Media devices
media_player:
  - platform: samsungtv
    host: !secret samsung_tv_ip
    mac: !secret samsung_tv_mac
    name: Livingroom TV
    port: 8001
  - platform: cast
    host: !secret chromecast_ip
    name: Livingroom Chromecast
  - platform: cast
    host: !secret google_home_ip
  - platform: plex

# Mosquitto set up running on HA Pi
mqtt:
  broker: core-mosquitto

# Device trackers
device_tracker:
  - platform: owntracks
    max_gps_accuracy: 200
    consider_home: 180
  # TODO: Work on the know devices list
  - platform: netgear
    host: !secret netgear_ip
    username: !secret netgear_username
    password: !secret netgear_password
    interval_seconds: 10
    consider_home: 180

# IFTT Maker channel
ifttt:
  key: !secret ifttt_maker_key

# Notifications
notify:
  - platform: pushbullet
    name: YAR
    api_key: !secret pushbullet_key

# Define zones for triggering actions
zone:
  name: Sofi's Work
  latitude: !secret sofi_work_latitude
  longitude: !secret sofi_work_longitude
  radius: 20
  icon: mdi:beer

zone 2:
  name: Georgi's Work
  latitude: !secret georgi_work_latitude
  longitude: !secret georgi_work_longitude
  icon: mdi:security

zone 3:
  name: Mr. President
  latitude: !secret mr_president_latitude
  longitude: !secret mr_president_longitude
  icon: mdi:memory

###############################################
# Includes
###############################################

# Automations
automation: !include_dir_merge_list automations/

# Cameras
camera: !include cameras.yaml

# Groups
group: !include groups.yaml

# Input select
input_select: !include input_select.yaml

# Sensors
sensor: !include sensors.yaml

# Switches
switch: !include switches.yaml

# Lights
light: !include lights.yaml

# Scenes
scene: !include scenes.yaml

input_number:
  office_animation_speed:
    name: Office Animation Speed
    initial: 150
    min: 1
    max: 150
    step: 10
  christmas_tree_animation_speed:
    name: Christmas Tree Animation Speed
    initial: 150
    min: 1
    max: 150
    step: 10