# Kubernetes Manifests for [Der-Henning/tgtg](https://github.com/Der-Henning/tgtg)

We all should be buying [@Der-Henning](https://github.com/Der-Henning) a coffe!

## Run

1. Create a `.env` file with your settings following [the official sample](https://github.com/Der-Henning/tgtg/blob/main/sample.env)
2. Make sure the path defined in [pv.yaml](pv.yaml#L14) exists in your nodes
3. Deploy with `kubectl -k apply ./`

## Troubleshoot

Delete everthing with `kubectl -k delete ./` and start digging :shrug:

Check the logs with `k get pods -n tgtg-scanner | tail -n1 | cut -d' ' -f1 | xargs -I@ kubectl logs -f @`
