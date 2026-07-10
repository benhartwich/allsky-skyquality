# Changelog

## v0.1.0

Initial release.

- Sky brightness in mag/arcsec² using `mag = offset − 2.5·log10(signal)`.
- Exposure- and gain-normalised signal so the reading tracks true sky brightness
  instead of the auto-exposure control loop.
- ROI via mask image, explicit rectangle, or central FOV divisor.
- Rough Bortle description alongside the numeric value.
- Rolling `skyquality.json` history for time-series charting.
- Environment variables `AS_SQM`, `AS_SQM_ADU`, `AS_SQM_DESC` for the overlay.

## v0.2.0

- Record extra sensor-free metrics alongside SQM: star count (cv2.matchTemplate,
  indi-allsky style, clear/cloudy ratio ~14x at threshold 0.65) and camera + CPU
  temperature. Written to skyquality.json as stars/temp/cpu.
- Expanded dashboard (web/skyquality.html): SQM, visible stars, camera temperature
  and meteors-per-night, each a themed SVG chart, no external libraries.

## v0.3.0

- Cloud/haze index (star-deficit grid) and aurora index (green-excess on the north
  horizon) added to skyquality.json, both sensor-free.
- Dashboard: cloud-cover chart, aurora candidate banner, tonight's active-shower
  context line.
