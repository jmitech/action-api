# action-api

## Usage

Print output:

```yaml
- name: Fetch data from jmitech-api
  uses: jmitech/action-api@v1
  with:
    url: https://api.mydomain.com/v1/health
    output: log
```

Save response to file:

```yaml
- name: Fetch data from jmitech-api
  uses: jmitech/action-api@v1
  with:
    url: https://api.mydomain.com/v1/net/device/ds98/ips
    output: ds13-ips.json
```

Custom jq filter/query:

```yaml
- name: Fetch data from jmitech-api and filter response
  uses: jmitech/action-api@v1
  with:
    url: https://api.mydomain.com/v1/vault/secret/kv/data/super-project/key/machines
    output: machines.json
    jq: .value.machines[]
```