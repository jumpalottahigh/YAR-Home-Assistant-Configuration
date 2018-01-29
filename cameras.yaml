# Shows Georgi and Sofi on a map.
- platform: generic
  name: Georgi's position
  still_image_url: https://maps.googleapis.com/maps/api/staticmap?center={{ states.device_tracker.username_gp.attributes.latitude }},{{ states.device_tracker.username_gp.attributes.longitude }}&zoom=15&size=500x500&maptype=roadmap&markers=color:blue%7Clabel:P%7C{{ states.device_tracker.username_gp.attributes.latitude }},{{ states.device_tracker.username_gp.attributes.longitude }}
  limit_refetch_to_url_change: true

- platform: generic
  name: Sofi's position
  still_image_url: https://maps.googleapis.com/maps/api/staticmap?center={{ states.device_tracker.username_sp.attributes.latitude }},{{ states.device_tracker.username_sp.attributes.longitude }}&zoom=15&size=500x500&maptype=roadmap&markers=color:blue%7Clabel:P%7C{{ states.device_tracker.username_sp.attributes.latitude }},{{ states.device_tracker.username_sp.attributes.longitude }}
  limit_refetch_to_url_change: true

- platform: mjpeg
  name: Antons room
  mjpeg_url: !secret camera_antons_room_ip_credentials