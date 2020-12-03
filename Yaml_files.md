# YAML (YANL Ain't Markup Language)

Why is YAML popular?

- configuration files all writen in YAML (Docker, Ansible, Kubernetes)
- widely used format
- human readable and intuitive

In general YAML is a data serialization language ( standard format to transfer data) like XML and JSON.

YAML

```yaml
microservices:
  - app: user-authentication
    port: 9000
    version: 1.0
```

XML

```xml
<microservices>
    <microservice>
        <app>user-authentication</app>
        <port>9000</port>
        <version>1.0</version>
    <microservice>
<microservices>
```

JSON

```json
{
  "microservices": [
    {
      "app": "user-authentication",
      "port": 9000,
      "version": "1.0"
    }
  ]
}
```

YMAL does not have special characters like <>, {}, [] you use line separation and indentation.

## Syntax

### Key-Value Pairs

```yaml
microservice:
  # comment here
  app: user-authentication
  port: 9000
  # comment here
  version: 1.7
  # boolean values
  deployed: yes
  deployed: true
  deployed: on
  # list
  list:
  - shopping
  - cart
```
