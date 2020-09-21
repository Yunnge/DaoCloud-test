<template>
  <div class="home">
    <div id="container"></div>
  </div>
</template>

<script>
import { Chart } from '@antv/g2';
import DataSet from '@antv/data-set';
import moment from "moment";
export default {
  name: 'home',

  mounted () {
    const jsonArr = [
      {
        "traceID": "356437af245fd4e1",
        "spanID": "286a0a8ecf380722",
        "flags": 1,
        "operationName": "HTTP GET /customer",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "66be4e8581d8682c"
          }
        ],
        "startTime": 1600334616864227,
        "duration": 287295,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/customer?customer=123"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334616864478,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/customer?customer=123"
              }
            ]
          },
          {
            "timestamp": 1600334616865170,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Loading customer"
              },
              {
                "key": "customer_id",
                "type": "string",
                "value": "123"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          }
        ],
        "processID": "p1",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "1bdfcf56e810b699",
        "flags": 1,
        "operationName": "HTTP GET: /customer",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334616862755,
        "duration": 289213,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "66be4e8581d8682c",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "1bdfcf56e810b699"
          }
        ],
        "startTime": 1600334616862779,
        "duration": 289043,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8081/customer?customer=123"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8081"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334616862954,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334616863111,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334616863403,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334616863486,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617151773,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617151881,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617151925,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "329e244e85539c28",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617355698,
        "duration": 5802,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T730540C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "3842f4fba078c110",
        "flags": 1,
        "operationName": "FindDriverIDs",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617153071,
        "duration": 22958,
        "tags": [
          {
            "key": "param.location",
            "type": "string",
            "value": "115,277"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617175836,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Found drivers"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          }
        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "1573f69d98e58b87",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617176114,
        "duration": 24993,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T719340C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "error",
            "type": "bool",
            "value": true
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617201030,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "driver_id",
                "type": "string",
                "value": "T719340C"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              }
            ]
          }
        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "6317f71ade2f4d4c",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617201689,
        "duration": 8371,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T719340C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "15b9443540fb3b13",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617210458,
        "duration": 10055,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T739069C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "4f9ee9e141a168df",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617220556,
        "duration": 9029,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T736841C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "6b7b35770672e2c6",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617280672,
        "duration": 9232,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T766508C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "10a8d6b35cab1846",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617242528,
        "duration": 26056,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T746252C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "error",
            "type": "bool",
            "value": true
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617268086,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "driver_id",
                "type": "string",
                "value": "T746252C"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              }
            ]
          }
        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "7ee6004718771a37",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617268969,
        "duration": 11552,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T746252C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "76e4cd4ce33fad6b",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617303459,
        "duration": 8678,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T773602C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "5e4ce0dbccbc213c",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617289943,
        "duration": 13284,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T786692C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0edee544c442e716",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617312194,
        "duration": 36634,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T733982C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "error",
            "type": "bool",
            "value": true
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617348675,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "driver_id",
                "type": "string",
                "value": "T733982C"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              }
            ]
          }
        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "2eae25688b2fee94",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617229642,
        "duration": 12852,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T788519C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0c3ff705adf6945c",
        "flags": 1,
        "operationName": "GetDriver",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "119bbcf9079a9382"
          }
        ],
        "startTime": 1600334617349516,
        "duration": 6122,
        "tags": [
          {
            "key": "param.driverID",
            "type": "string",
            "value": "T733982C"
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p3",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "58c3afff87533859",
        "flags": 1,
        "operationName": "SQL SELECT",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "286a0a8ecf380722"
          }
        ],
        "startTime": 1600334616866794,
        "duration": 284691,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "peer.service",
            "type": "string",
            "value": "mysql"
          },
          {
            "key": "sql.query",
            "type": "string",
            "value": "SELECT * FROM customer WHERE customer_id=123"
          },
          {
            "key": "request",
            "type": "string",
            "value": "2002-1"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334616867003,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Acquired lock with 0 transactions waiting behind"
              }
            ]
          }
        ],
        "processID": "p4",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "2600d31eaf631c5f",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "49a2b0a29751014b"
          }
        ],
        "startTime": 1600334617364583,
        "duration": 42606,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=588%2C127"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617364643,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=588%2C127"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0a3a6b6200f56e41",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "2875913e6ca5de7e"
          }
        ],
        "startTime": 1600334617364104,
        "duration": 43088,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=982%2C258"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617364206,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=982%2C258"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "62dd5259bf62c9a1",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "50b86aa001bfa86d"
          }
        ],
        "startTime": 1600334617364049,
        "duration": 53185,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=785%2C547"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617364172,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=785%2C547"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "6c2856ddabc656a2",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "72e332a014c90580"
          }
        ],
        "startTime": 1600334617409607,
        "duration": 44960,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=113%2C556"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617409650,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=113%2C556"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "45551b57d9660c5f",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "69134cd0dee46074"
          }
        ],
        "startTime": 1600334617412392,
        "duration": 60989,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=623%2C496"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617412439,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=623%2C496"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "016470f959f4842b",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "67a00d7bc1cb9bbd"
          }
        ],
        "startTime": 1600334617418922,
        "duration": 63175,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=337%2C566"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617418957,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=337%2C566"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "58607fb5f654676d",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "20fcc23c5c203480"
          }
        ],
        "startTime": 1600334617459188,
        "duration": 43359,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=461%2C246"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617459253,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=461%2C246"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "57e76e8cb379a7fa",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "4c89770cb87b32d5"
          }
        ],
        "startTime": 1600334617483370,
        "duration": 43685,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=590%2C884"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617483403,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=590%2C884"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "5cb58da2b735d502",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "7e73c8739be1032e"
          }
        ],
        "startTime": 1600334617474858,
        "duration": 53402,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=740%2C440"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617475006,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=740%2C440"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "61a1c0ac5dd2b219",
        "flags": 1,
        "operationName": "HTTP GET /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "4ea90c199e8fba33"
          }
        ],
        "startTime": 1600334617507238,
        "duration": 44952,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/route?dropoff=115%2C277&pickup=752%2C222"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617507396,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/route?dropoff=115%2C277&pickup=752%2C222"
              }
            ]
          }
        ],
        "processID": "p5",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "119bbcf9079a9382",
        "flags": 1,
        "operationName": "/driver.DriverService/FindNearest",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "1c19de7cb668bc56"
          }
        ],
        "startTime": 1600334617152939,
        "duration": 208853,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "component",
            "type": "string",
            "value": "gRPC"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617152979,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Searching for nearby drivers"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "location",
                "type": "string",
                "value": "115,277"
              }
            ]
          },
          {
            "timestamp": 1600334617201476,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Retrying GetDriver after error"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              },
              {
                "key": "retry_no",
                "type": "int64",
                "value": 1
              }
            ]
          },
          {
            "timestamp": 1600334617268732,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Retrying GetDriver after error"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              },
              {
                "key": "retry_no",
                "type": "int64",
                "value": 1
              }
            ]
          },
          {
            "timestamp": 1600334617348873,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Retrying GetDriver after error"
              },
              {
                "key": "error",
                "type": "string",
                "value": "redis timeout"
              },
              {
                "key": "level",
                "type": "string",
                "value": "error"
              },
              {
                "key": "retry_no",
                "type": "int64",
                "value": 1
              }
            ]
          },
          {
            "timestamp": 1600334617361558,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Search successful"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "num_drivers",
                "type": "int64",
                "value": 10
              }
            ]
          }
        ],
        "processID": "p6",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "1c19de7cb668bc56",
        "flags": 1,
        "operationName": "/driver.DriverService/FindNearest",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617152246,
        "duration": 210174,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "gRPC"
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "49a2b0a29751014b",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "250c34a1ae1c95a7"
          }
        ],
        "startTime": 1600334617362935,
        "duration": 45301,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=588%2C127"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": false
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": false
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617363004,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617363188,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectStart"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363503,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectDone"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363577,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617364092,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617364156,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617407835,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617408137,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617408198,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "250c34a1ae1c95a7",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617362895,
        "duration": 45376,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "2875913e6ca5de7e",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "0d9cf220999e6c3d"
          }
        ],
        "startTime": 1600334617363113,
        "duration": 46342,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=982%2C258"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": false
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": false
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617363159,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617363533,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectStart"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363795,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectDone"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363868,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617363927,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617363953,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617408217,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617408838,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617409099,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0d9cf220999e6c3d",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617363083,
        "duration": 46400,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "50b86aa001bfa86d",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "7ffed8055d7f94d2"
          }
        ],
        "startTime": 1600334617362815,
        "duration": 55233,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=785%2C547"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": false
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": false
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617362881,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617363113,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectStart"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363519,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ConnectDone"
              },
              {
                "key": "addr",
                "type": "string",
                "value": "0.0.0.0:8083"
              },
              {
                "key": "network",
                "type": "string",
                "value": "tcp"
              }
            ]
          },
          {
            "timestamp": 1600334617363577,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617363719,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617363746,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617417805,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617417967,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617418023,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "7ffed8055d7f94d2",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617362773,
        "duration": 55295,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "72e332a014c90580",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "1cc51a8bc370c48f"
          }
        ],
        "startTime": 1600334617408784,
        "duration": 47536,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=113%2C556"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617408853,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617408983,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617409085,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617409118,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617455256,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617456025,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617456208,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "1cc51a8bc370c48f",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617408750,
        "duration": 47844,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "69134cd0dee46074",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "7a042dbc2813f28c"
          }
        ],
        "startTime": 1600334617410702,
        "duration": 63018,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=623%2C496"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617410923,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617411145,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617411727,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617411755,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617473577,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617473663,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617473710,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "7a042dbc2813f28c",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617410487,
        "duration": 63253,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "67a00d7bc1cb9bbd",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "023767650ede5b27"
          }
        ],
        "startTime": 1600334617418398,
        "duration": 64085,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=337%2C566"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617418472,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617418541,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617418748,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617418773,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617482238,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617482435,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617482472,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "023767650ede5b27",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617418363,
        "duration": 64131,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "20fcc23c5c203480",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "0189e906bbd6372c"
          }
        ],
        "startTime": 1600334617457161,
        "duration": 45890,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=461%2C246"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617457238,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617457431,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617458619,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617458732,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617502787,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617502957,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617503024,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0189e906bbd6372c",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617456991,
        "duration": 46101,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "4c89770cb87b32d5",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "0d50056963ce2aad"
          }
        ],
        "startTime": 1600334617482615,
        "duration": 44908,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=590%2C884"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617482734,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617482777,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617482826,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617482840,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617493768,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617493851,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617493895,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "0d50056963ce2aad",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617482595,
        "duration": 44950,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "7e73c8739be1032e",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "13d915a17625ade7"
          }
        ],
        "startTime": 1600334617473915,
        "duration": 54788,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=740%2C440"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617473961,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617474004,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617474052,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617474071,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617494935,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617495021,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617495075,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "13d915a17625ade7",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617473889,
        "duration": 54834,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "71a4590a2bb7b5e2",
        "flags": 1,
        "operationName": "HTTP GET: /route",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "356437af245fd4e1"
          }
        ],
        "startTime": 1600334617506173,
        "duration": 46781,
        "tags": [
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [

        ],
        "processID": "p2",
        "warnings": null
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "356437af245fd4e1",
        "flags": 1,
        "operationName": "HTTP GET /dispatch",
        "references": [

        ],
        "startTime": 1600334616862142,
        "duration": 691127,
        "tags": [
          {
            "key": "sampler.type",
            "type": "string",
            "value": "const"
          },
          {
            "key": "sampler.param",
            "type": "bool",
            "value": true
          },
          {
            "key": "span.kind",
            "type": "string",
            "value": "server"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "/dispatch?customer=123&nonse=0.7337089878922212"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334616862188,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "HTTP request received"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "method",
                "type": "string",
                "value": "GET"
              },
              {
                "key": "url",
                "type": "string",
                "value": "/dispatch?customer=123&nonse=0.7337089878922212"
              }
            ]
          },
          {
            "timestamp": 1600334616862544,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Getting customer"
              },
              {
                "key": "customer_id",
                "type": "string",
                "value": "123"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          },
          {
            "timestamp": 1600334617151997,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Found customer"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          },
          {
            "timestamp": 1600334617152077,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "baggage"
              },
              {
                "key": "key",
                "type": "string",
                "value": "customer"
              },
              {
                "key": "value",
                "type": "string",
                "value": "Rachel's Floral Designs"
              }
            ]
          },
          {
            "timestamp": 1600334617152098,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding nearest drivers"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "location",
                "type": "string",
                "value": "115,277"
              }
            ]
          },
          {
            "timestamp": 1600334617362458,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Found drivers"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          },
          {
            "timestamp": 1600334617362590,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "785,547"
              }
            ]
          },
          {
            "timestamp": 1600334617362787,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "588,127"
              }
            ]
          },
          {
            "timestamp": 1600334617362980,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "982,258"
              }
            ]
          },
          {
            "timestamp": 1600334617408502,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "113,556"
              }
            ]
          },
          {
            "timestamp": 1600334617409527,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "623,496"
              }
            ]
          },
          {
            "timestamp": 1600334617418106,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "337,566"
              }
            ]
          },
          {
            "timestamp": 1600334617456658,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "461,246"
              }
            ]
          },
          {
            "timestamp": 1600334617473775,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "740,440"
              }
            ]
          },
          {
            "timestamp": 1600334617482521,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "590,884"
              }
            ]
          },
          {
            "timestamp": 1600334617503129,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Finding route"
              },
              {
                "key": "dropoff",
                "type": "string",
                "value": "115,277"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              },
              {
                "key": "pickup",
                "type": "string",
                "value": "752,222"
              }
            ]
          },
          {
            "timestamp": 1600334617519388,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Found routes"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          },
          {
            "timestamp": 1600334617519526,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "Dispatch successful"
              },
              {
                "key": "driver",
                "type": "string",
                "value": "T739069C"
              },
              {
                "key": "eta",
                "type": "string",
                "value": "2m0s"
              },
              {
                "key": "level",
                "type": "string",
                "value": "info"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": [
          "Invalid span reference removed {TraceID:0000000000000000 SpanID:0000000000000000 RefType:CHILD_OF XXX_NoUnkeyedLiteral:{} XXX_unrecognized:[] XXX_sizecache:0}"
        ]
      },
      {
        "traceID": "356437af245fd4e1",
        "spanID": "4ea90c199e8fba33",
        "flags": 1,
        "operationName": "HTTP GET",
        "references": [
          {
            "refType": "CHILD_OF",
            "traceID": "356437af245fd4e1",
            "spanID": "71a4590a2bb7b5e2"
          }
        ],
        "startTime": 1600334617506222,
        "duration": 46709,
        "tags": [
          {
            "key": "span.kind",
            "type": "string",
            "value": "client"
          },
          {
            "key": "component",
            "type": "string",
            "value": "net/http"
          },
          {
            "key": "http.method",
            "type": "string",
            "value": "GET"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=752%2C222"
          },
          {
            "key": "http.url",
            "type": "string",
            "value": "0.0.0.0:8083"
          },
          {
            "key": "net/http.reused",
            "type": "bool",
            "value": true
          },
          {
            "key": "net/http.was_idle",
            "type": "bool",
            "value": true
          },
          {
            "key": "http.status_code",
            "type": "int64",
            "value": 200
          },
          {
            "key": "internal.span.format",
            "type": "string",
            "value": "proto"
          }
        ],
        "logs": [
          {
            "timestamp": 1600334617506463,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GetConn"
              }
            ]
          },
          {
            "timestamp": 1600334617506567,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotConn"
              }
            ]
          },
          {
            "timestamp": 1600334617506750,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteHeaders"
              }
            ]
          },
          {
            "timestamp": 1600334617506784,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "WroteRequest"
              }
            ]
          },
          {
            "timestamp": 1600334617518975,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "GotFirstResponseByte"
              }
            ]
          },
          {
            "timestamp": 1600334617519178,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "PutIdleConn"
              }
            ]
          },
          {
            "timestamp": 1600334617519305,
            "fields": [
              {
                "key": "event",
                "type": "string",
                "value": "ClosedBody"
              }
            ]
          }
        ],
        "processID": "p2",
        "warnings": null
      }
    ];


    jsonArr.sort(function (a, b) {
      return a.startTime > b.startTime ? 1 : -1
    });


    for (let item of jsonArr) {
      item.startTime = moment(item.startTime).format("YYYY-MM-DD HH:mm:ss");
      item.operationName = 'frontend：' + item.operationName
    }

    let data = this.merger(jsonArr)

    console.log(data)

    // console.log(data)

    const ds = new DataSet();
    const dv = ds.createView().source(data);
    dv.transform({
      type: 'map',
      callback: function callback (row) {
        const times = row.startTime.split(' ');
        row.time = times[1];
        return row;
      }
    });

    const chart = new Chart({
      container: 'container',
      autoFit: true,
      height: 500,
      padding: [50, 50, 50, 100],
    });
    chart.data(dv.rows);

    chart.scale({
      time: {
        alias: 'Time', // 定义别名
        // tickInterval: 5, // 自定义刻度间距
        // type: 'cat',
        tickCount: 10
      },
      date: {
        type: 'cat'
      },
      duration: {
        alias: 'Duration',
        // tickCount: 6
        // max: 165,
        // min: 0
      },
    });
    // 开始配置坐标轴
    chart.axis('time', {
      title: {
        offset: 40
      },
      label: {
        formatter: val => {
          return val + ' pm'; // 格式化坐标轴显示文本
        }
      },
      grid: {
        line: {
          style: {
            stroke: '#d9d9d9',
            lineWidth: 0,
            lineDash: [2, 2]
          }
        }
      }
    });
    chart.axis('duration', {
      title: {
        offset: 80
      },
      label: {
        formatter: val => {
          if (+val > 0) {
            return val + ' ms';
          } else {
            return val;
          }
        }
      },
      grid: {
        line: {
          style: {
            stroke: '#d9d9d9',
            lineWidth: 0,
            lineDash: [1, 1]
          }
        }
      }
    });
    chart.legend(false);
    chart.tooltip({
      title: 'operationName',
      showMarkers: false,
    });
    chart
      .point()
      .position('time*duration')
      .color('#42b983')
      .size('duration', [5, 40])
      .shape('circle')
      .tooltip('duration')
      .style({
        lineWidth: 0,
        stroke: '#42b983',
        fillOpacity: 0.4,
      });
    // chart.annotation().line({
    //   top: true,
    //   start: [65, 'min'],
    //   end: [65, 'max'],
    //   text: {
    //     content: 'Safe fat intake 65g/day',
    //     position: 'end',
    //     autoRotate: false,
    //     style: {
    //       textAlign: 'start'
    //     }
    //   }
    // });
    // chart.annotation().line({
    //   top: true,
    //   start: ['min', 50],
    //   end: ['max', 50],
    //   text: {
    //     content: 'Safe sugar intake 50g/day',
    //     position: 'end',
    //     style: {
    //       textAlign: 'end'
    //     }
    //   }
    // });
    chart.annotation().region({
      start: ['0%', '0%'],
      end: ['100%', '100%'],
      style: {
        lineWidth: 0.5,
        fillOpacity: 0,
        strokeOpacity: 1,
        stroke: '#999',
      }
    });

    // chart.coordinate() 

    chart.interaction('element-active');

    chart.render();

  },

  methods: {
    merger (arr) {
      let tempArr = [],
        newArr = [];
      for (let i = 0; i < arr.length; i++) {
        if (tempArr.indexOf(arr[i].startTime) === -1) {
          newArr.push({
            startTime: arr[i].startTime,
            duration: arr[i].duration,
            operationName: arr[i].operationName
          });
          tempArr.push(arr[i].startTime);
        } else {
          for (let j = 0; j < newArr.length; j++) {
            if (newArr[j].startTime == arr[i].startTime) {
              newArr[j].duration += arr[i].duration
            }
          }
        }
      }
      return newArr;
    }
  }
}
</script>
