swagger: "2.0"
x-collection-name: DomainTools
x-complete: 1
info:
  title: Whois Lookup API
  version: 1.0.0
host: api.domaintools.com
basePath: /v1/domaintools.com/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /mark-alert/:
    get:
      summary: Brand Monitor
      description: Monitor new domains registrations for specific keywords
      operationId: brandMonitor
      x-api-path-slug: markalert-get
      parameters:
      - in: query
        name: days_back
        description: Use this parameter in exceptional circumstances where you need
          to search domains registered up to six days prior to the current date
        type: string
        format: string
      - in: query
        name: domain_status
        description: Sets the scope of domain names to search
        type: string
        format: string
      - in: query
        name: exclude
        description: Domain names with these words will be excluded from the result
          set
        type: string
        format: string
      - in: query
        name: query
        description: One or more terms separated by the pipe character ( | )
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Brand Monitor