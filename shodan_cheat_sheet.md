# Shodan Cheat Sheet

## Common General Search Filters

| Filter        | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `ip:`         | Filter results by specific IP address.                              |
| `asn:`        | Filter results by specific ASN ID.                                  |
| `hostname:`   | Filter results by specific hostname.                                |
| `port:`       | Filter results by specific port number of service.                  |
| `net:`        | Filter results from specified CIDR block.                           |
| `isp:`        | Filter results by devices assigned a particular address (space) from a specified ISP. |
| `city:`       | Filter results by specific city.                                    |
| `country:`    | Filter results by specific two-digit country code.                  |
| `os:`         | Filter results by particular OS.                                    |
| `product:`    | Filter results by particular software.                              |
| `version:`    | Filter results by specified version of software.                    |

## Common Premium API Search Filters

| Filter        | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `vuln:`       | Filter results by particular vulnerability ID (commonly CVE).       |
| `tag:`        | Filter results by tags on device.                                   |

## HTTP Filters

| Filter        | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `http.component:` | Filter results by a particular web technology.                   |
| `http.status:`    | Filter results by specific status code.                         |
| `http.html:`      | Filter results by strings found in HTML of files served.         |
| `http.title:`     | Filter results by string found in title of web pages served.     |

## Common CLI Commands

| Command       | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `count`       | Returns the number of results for a search.                         |
| `domain`      | View all available information for a domain.                        |
| `download`    | Download search results and save them in a compressed JSON file.    |
| `honeyscore`  | Check whether the IP is a honeypot or not.                          |
| `host`        | View all available information for an IP address.                  |
| `parse`       | Extract information out of compressed JSON files.                  |
| `scan`        | Scan an IP/netblock using Shodan.                                   |
| `search`      | Search the Shodan database.                                         |

## Common CLI Search Fields

| Field         | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `ip_str`      | Displays the IP string upon a search.                               |
| `port`        | Displays the port number upon a search.                             |
| `org`         | Displays the organization name upon a search.                       |
| `hostnames`   | Displays hostnames upon a search.                                   |
| `os`          | Displays the operating system upon a search.                        |
| `country`     | Displays the country code upon a search.                            |
| `city`        | Displays the city name upon a search.                               |

## Common CLI Stats Facets

| Facet         | Description                                                         |
|---------------|---------------------------------------------------------------------|
| `asn`         | Returns statistical information about ASN.                          |
| `city`        | Returns statistical information about cities.                       |
| `country`     | Returns statistical information about countries.                    |
| `cloud.provider` | Returns statistical information about cloud providers.           |
| `cloud.service`  | Returns statistical information about cloud services.            |
| `device`      | Returns statistical information about devices.                     |
| `domain`      | Returns statistical information about domains.                     |
| `ip`          | Returns statistical information about IP addresses.                |
| `org`         | Returns statistical information about organizations.               |
| `os`          | Returns statistical information about operating systems.           |
| `version`     | Returns statistical information about software versions.           |

