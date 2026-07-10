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
