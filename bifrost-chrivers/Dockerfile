ARG BUILD_FROM
FROM $BUILD_FROM

# This add-on runs the old chrivers-based Bifrost, which cannot read the state
# file of newer versions. It therefore uses its own directory. On first start,
# config.yaml and cert.pem are copied from /config/bifrost, so the bridge keeps
# its identity, while the state (state.yaml) starts fresh.

WORKDIR /config/bifrost-legacy

CMD ["/bin/sh", "-c", "for f in config.yaml cert.pem; do [ -f \"$f\" ] || cp \"/config/bifrost/$f\" . 2>/dev/null || true; done; exec /app/bifrost"]
