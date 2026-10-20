# Bifrost (chrivers)

Bifrost built from the `chrivers` branch of
[0xvisualiris/bifrost](https://github.com/0xvisualiris/bifrost/tree/chrivers):
the original chrivers/bifrost code with the entertainment-mode fix.

- Uses its own directory `/config/bifrost-legacy`. On first start,
  `config.yaml` and `cert.pem` are copied from `/config/bifrost`.
- The state starts fresh: the Hue app and Hue Sync clients (TV) must be paired
  again, and entertainment areas must be created again.
- Do not run this add-on at the same time as "Bifrost" or "Bifrost Dev"; they
  use the same ports.
