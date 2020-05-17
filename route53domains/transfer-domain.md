# Transfer domain

Start a transfer:

```sh
aws route53domains \
transfer-domain-to-another-aws-account \
--domain-name example.com \
--account-id 000000000000 
```

Output:

```
{
    "OperationId": "c3fefe98-5543-4d65-beb4-1a865e5c67d6",
    "Password": "…"
}
```

Complete a transfer:

```sh
aws route53domains \
accept-domain-transfer-from-another-aws-account \
--domain-name example.com \
--password "…" \
--region us-east-1
```

Output:

```
{
    "OperationId": "6bb64e0f-615c-4e37-afed-e7369ba31560"
}
```
