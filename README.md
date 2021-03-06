# Bind DNS Graylog Extractor

## Example log

`06-Mar-2021 13:34:44.911 queries: info: client 10.9.9.3#35510 (www.bilecik.edu.tr): query: www.bilecik.edu.tr IN A -EDC (192.168.1.1)`
## Grok pattern
`%{MONTHDAY}-%{MONTH}-%{YEAR} %{TIME} queries: info: client %{IPV4:client_ip}%{DATA} \(%{DATA:query}\)`

## Extracted fields
* MONTHDAY
* MONTH
* YEAR
* TIME
* HOUR
* MINUTE
* SECOND
* client_ip
* query

## Result

```json
{
  "MONTHDAY": [
    [
      "06"
    ]
  ],
  "MONTH": [
    [
      "Mar"
    ]
  ],
  "YEAR": [
    [
      "2021"
    ]
  ],
  "TIME": [
    [
      "13:34:44.911"
    ]
  ],
  "HOUR": [
    [
      "13"
    ]
  ],
  "MINUTE": [
    [
      "34"
    ]
  ],
  "SECOND": [
    [
      "44.911"
    ]
  ],
  "client_ip": [
    [
      "10.9.9.3"
    ]
  ],
  "DATA": [
    [
      "#35510"
    ]
  ],
  "query": [
    [
      "www.bilecik.edu.tr"
    ]
  ]
}
```
