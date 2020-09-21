<template>
  <div class="charts">
    <!-- 布局 -->
    <div class="header">
      <div class="menu-top">Service&Operration</div>
      <div class="time">
        <div class="time-scale" v-for="(item, index) in timeList" :key="index">
          <span>{{item}}ms</span>
          <span v-if="index == 3">
            {{maxVal}}ms
          </span>
        </div>
      </div>
    </div>
    <div class="bar-chart">
      <div class="bar-list" v-for="(item, index) in lists" :key="index">
        <!-- 名称 -->
        <div class="menu-bar">{{item.operationName}}</div>
        <!-- 画条形图 -->
        <div class="rectangle-bar">
          <div class="color-bar" 
          :style="{width: item.duration/maxVal*100 + '%',  marginLeft: item.dValue/maxVal*100 + '%', background: item.color}">
            <span :class="item.dValue/maxVal > 0.5?'bar-value-left':'bar-value'">{{item.duration}}ms</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import moment from "moment";

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      "lists": [
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "4ed0b18329f0b3b1",
          "flags": 1,
          "operationName": "HTTP GET /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "50e4b1027879100c"
            }
          ],
          "startTime": 1600334616000273,
          "duration": 65817,
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
              "value": "/route?dropoff=115%2C277&pickup=332%2C541"
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
              "timestamp": 1600334616000462,
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
                  "value": "/route?dropoff=115%2C277&pickup=332%2C541"
                }
              ]
            }
          ],
          "processID": "p1",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "6514fa94c49ed636",
          "flags": 1,
          "operationName": "HTTP GET /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "79dc30bc2bd1f7ea"
            }
          ],
          "startTime": 1600334616004783,
          "duration": 65199,
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
              "value": "/route?dropoff=115%2C277&pickup=136%2C584"
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
              "timestamp": 1600334616004853,
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
                  "value": "/route?dropoff=115%2C277&pickup=136%2C584"
                }
              ]
            }
          ],
          "processID": "p1",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "03319e16893c8f18",
          "flags": 1,
          "operationName": "HTTP GET /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "3e7ce85003dc6e5c"
            }
          ],
          "startTime": 1600334616003474,
          "duration": 76743,
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
              "value": "/route?dropoff=115%2C277&pickup=628%2C41"
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
              "timestamp": 1600334616004243,
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
                  "value": "/route?dropoff=115%2C277&pickup=628%2C41"
                }
              ]
            }
          ],
          "processID": "p1",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "2ced3b1a374319d1",
          "flags": 1,
          "operationName": "HTTP GET /customer",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "7bbba034653e8885"
            }
          ],
          "startTime": 1600334615438230,
          "duration": 339272,
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
              "timestamp": 1600334615438308,
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
              "timestamp": 1600334615446875,
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
          "processID": "p2",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "17c8fb34b1afd806",
          "flags": 1,
          "operationName": "/driver.DriverService/FindNearest",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "112c0818fb89e2dd"
            }
          ],
          "startTime": 1600334615779610,
          "duration": 215143,
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
              "timestamp": 1600334615779638,
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
              "timestamp": 1600334615858027,
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
              "timestamp": 1600334615938775,
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
              "timestamp": 1600334615994093,
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
          "processID": "p3",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "7bbba034653e8885",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "5a41632410ef762a"
            }
          ],
          "startTime": 1600334615437494,
          "duration": 340479,
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
              "timestamp": 1600334615437553,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GetConn"
                }
              ]
            },
            {
              "timestamp": 1600334615437810,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GotConn"
                }
              ]
            },
            {
              "timestamp": 1600334615437926,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteHeaders"
                }
              ]
            },
            {
              "timestamp": 1600334615437942,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteRequest"
                }
              ]
            },
            {
              "timestamp": 1600334615777692,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GotFirstResponseByte"
                }
              ]
            },
            {
              "timestamp": 1600334615777880,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "PutIdleConn"
                }
              ]
            },
            {
              "timestamp": 1600334615777940,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "ClosedBody"
                }
              ]
            }
          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "5a41632410ef762a",
          "flags": 1,
          "operationName": "HTTP GET: /customer",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334615437396,
          "duration": 340615,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "112c0818fb89e2dd",
          "flags": 1,
          "operationName": "/driver.DriverService/FindNearest",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334615778702,
          "duration": 218334,
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
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "50e4b1027879100c",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "69ce706de56b6da7"
            }
          ],
          "startTime": 1600334615999099,
          "duration": 38395,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=332%2C541"
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
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [
            {
              "timestamp": 1600334615999678,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GetConn"
                }
              ]
            },
            {
              "timestamp": 1600334615999757,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GotConn"
                }
              ]
            },
            {
              "timestamp": 1600334615999891,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteHeaders"
                }
              ]
            },
            {
              "timestamp": 1600334615999937,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteRequest"
                }
              ]
            }
          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "69ce706de56b6da7",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334615998229,
          "duration": 38911,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "3e7ce85003dc6e5c",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "0d3677a070e11933"
            }
          ],
          "startTime": 1600334615999871,
          "duration": 37525,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=628%2C41"
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
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [
            {
              "timestamp": 1600334616000503,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GetConn"
                }
              ]
            },
            {
              "timestamp": 1600334616000692,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GotConn"
                }
              ]
            },
            {
              "timestamp": 1600334616000777,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteHeaders"
                }
              ]
            },
            {
              "timestamp": 1600334616000820,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteRequest"
                }
              ]
            }
          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "51d6e326b918d566",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616001279,
          "duration": 36576,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "79dc30bc2bd1f7ea",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "51d6e326b918d566"
            }
          ],
          "startTime": 1600334616001311,
          "duration": 36525,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=136%2C584"
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
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [
            {
              "timestamp": 1600334616001355,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GetConn"
                }
              ]
            },
            {
              "timestamp": 1600334616002790,
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
              "timestamp": 1600334616003967,
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
              "timestamp": 1600334616004434,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "GotConn"
                }
              ]
            },
            {
              "timestamp": 1600334616004555,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteHeaders"
                }
              ]
            },
            {
              "timestamp": 1600334616004586,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "WroteRequest"
                }
              ]
            }
          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "0d3677a070e11933",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334615999783,
          "duration": 37793,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "4afcdf65681d3812",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616038047,
          "duration": 84,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "192b6a0601d6b6c6",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "522e01e465ec70cf"
            }
          ],
          "startTime": 1600334616039507,
          "duration": 158,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=490%2C871"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "3ef2f852690827ae",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "4afcdf65681d3812"
            }
          ],
          "startTime": 1600334616038074,
          "duration": 38,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=119%2C664"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "522e01e465ec70cf",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616039480,
          "duration": 204,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "59ce4581fa9c7028",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "6a4fd60f41b15289"
            }
          ],
          "startTime": 1600334616040748,
          "duration": 195,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=163%2C208"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "508488ed40f3845a",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "620ad099318d4001"
            }
          ],
          "startTime": 1600334616042450,
          "duration": 118,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=741%2C730"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "6a4fd60f41b15289",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616040674,
          "duration": 235,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "620ad099318d4001",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616042087,
          "duration": 323,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "031f81fef86613dd",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "55e082576574d826"
            }
          ],
          "startTime": 1600334616043763,
          "duration": 202,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=500%2C30"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "55e082576574d826",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616043723,
          "duration": 321,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "0b424da39ee29e8b",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "220bcf31adc15967"
            }
          ],
          "startTime": 1600334616044779,
          "duration": 40,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=65%2C517"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "46f4fcfbf8166ab0",
          "flags": 1,
          "operationName": "HTTP GET",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "11a287538aaf927e"
            }
          ],
          "startTime": 1600334616045166,
          "duration": 40,
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
              "value": "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=825%2C491"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "220bcf31adc15967",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616044752,
          "duration": 126,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "238d0a1ff5dde851",
          "flags": 1,
          "operationName": "HTTP GET /dispatch",
          "references": [

          ],
          "startTime": 1600334615434188,
          "duration": 611794,
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
              "value": "/dispatch?customer=123&nonse=0.07975472398284178"
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
              "timestamp": 1600334615434234,
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
                  "value": "/dispatch?customer=123&nonse=0.07975472398284178"
                }
              ]
            },
            {
              "timestamp": 1600334615435782,
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
              "timestamp": 1600334615778050,
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
              "timestamp": 1600334615778257,
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
              "timestamp": 1600334615778488,
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
              "timestamp": 1600334615997100,
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
              "timestamp": 1600334615997558,
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
                  "value": "136,584"
                }
              ]
            },
            {
              "timestamp": 1600334615997752,
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
                  "value": "332,541"
                }
              ]
            },
            {
              "timestamp": 1600334615998275,
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
                  "value": "628,41"
                }
              ]
            },
            {
              "timestamp": 1600334616037554,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=332%2C541": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616037612,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=628%2C41": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616037680,
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
                  "value": "119,664"
                }
              ]
            },
            {
              "timestamp": 1600334616037891,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=136%2C584": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616038157,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=119%2C664": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616038417,
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
                  "value": "490,871"
                }
              ]
            },
            {
              "timestamp": 1600334616039709,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=490%2C871": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616039913,
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
                  "value": "163,208"
                }
              ]
            },
            {
              "timestamp": 1600334616040977,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=163%2C208": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616041238,
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
                  "value": "741,730"
                }
              ]
            },
            {
              "timestamp": 1600334616042781,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=741%2C730": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616042933,
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
                  "value": "500,30"
                }
              ]
            },
            {
              "timestamp": 1600334616044177,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=500%2C30": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616044295,
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
                  "value": "65,517"
                }
              ]
            },
            {
              "timestamp": 1600334616044905,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=65%2C517": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616045000,
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
                  "value": "825,491"
                }
              ]
            },
            {
              "timestamp": 1600334616045246,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Error getting route"
                },
                {
                  "key": "error",
                  "type": "string",
                  //                                     "value":"Get "http://0.0.0.0:8083/route?dropoff=115%2C277&pickup=825%2C491": context canceled"
                },
                {
                  "key": "level",
                  "type": "string",
                  "value": "error"
                }
              ]
            },
            {
              "timestamp": 1600334616045346,
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
            }
          ],
          "processID": "p4",
          "warnings": [
            "Invalid span reference removed {TraceID:0000000000000000 SpanID:0000000000000000 RefType:CHILD_OF XXX_NoUnkeyedLiteral:{} XXX_unrecognized:[] XXX_sizecache:0}"
          ]
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "11a287538aaf927e",
          "flags": 1,
          "operationName": "HTTP GET: /route",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "238d0a1ff5dde851"
            }
          ],
          "startTime": 1600334616045092,
          "duration": 134,
          "tags": [
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [

          ],
          "processID": "p4",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "091a56f8a4fbcc13",
          "flags": 1,
          "operationName": "SQL SELECT",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "2ced3b1a374319d1"
            }
          ],
          "startTime": 1600334615449032,
          "duration": 328199,
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
              "value": "1004-11"
            },
            {
              "key": "internal.span.format",
              "type": "string",
              "value": "proto"
            }
          ],
          "logs": [
            {
              "timestamp": 1600334615449058,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "Acquired lock with 0 transactions waiting behind"
                }
              ]
            }
          ],
          "processID": "p5",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "793cb1c10e8c7370",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615883889,
          "duration": 10106,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T757410C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "77b0c2e67b5aecd1",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615808779,
          "duration": 14788,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T714394C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "2b6b919c39f45c6e",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615894028,
          "duration": 8777,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T703007C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "605bbd9d61a5ab52",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615823614,
          "duration": 34332,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T779041C"
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
              "timestamp": 1600334615857762,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "redis timeout"
                },
                {
                  "key": "driver_id",
                  "type": "string",
                  "value": "T779041C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "672a2ed7a555452c",
          "flags": 1,
          "operationName": "FindDriverIDs",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615779862,
          "duration": 15756,
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
              "timestamp": 1600334615795416,
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "63a6fb2504670960",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615902839,
          "duration": 35882,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T761504C"
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
              "timestamp": 1600334615938502,
              "fields": [
                {
                  "key": "event",
                  "type": "string",
                  "value": "redis timeout"
                },
                {
                  "key": "driver_id",
                  "type": "string",
                  "value": "T761504C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "387e2f7d915a3277",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615858265,
          "duration": 12097,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T779041C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "3d3229dc3065fbc6",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615795672,
          "duration": 13026,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T757047C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "23bf50eba6232c66",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615938897,
          "duration": 5832,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T761504C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "2db7ad38705b8c39",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615870503,
          "duration": 13292,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T772131C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "708aaeea93539ac1",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615959837,
          "duration": 15753,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T764389C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "095a2469355f9740",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615975734,
          "duration": 18291,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T779859C"
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
          "processID": "p6",
          "warnings": null
        },
        {
          "traceID": "238d0a1ff5dde851",
          "spanID": "6e2b4b1faa136f0a",
          "flags": 1,
          "operationName": "GetDriver",
          "references": [
            {
              "refType": "CHILD_OF",
              "traceID": "238d0a1ff5dde851",
              "spanID": "17c8fb34b1afd806"
            }
          ],
          "startTime": 1600334615944767,
          "duration": 14833,
          "tags": [
            {
              "key": "param.driverID",
              "type": "string",
              "value": "T760946C"
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
          "processID": "p6",
          "warnings": null
        }
      ],
      timeList: []
    }
  },

  computed: {
    // 求最大值
    maxVal () {
      return Math.max(...this.lists.map(x => x.duration));
    }
  },

  created () {
    let max = this.maxVal;
    if (max) {
      for (let i = 0; i < 4; i++) {
        this.timeList.push(this.numDot(i / 4 * max))
      }
    }

    // 排序
    this.lists.sort(function (a, b) {
      return a.startTime > b.startTime ? 1 : -1
    });


    for (let item of this.lists) {
      item.startTime = moment(item.startTime).format("YYYY-MM-DD HH:mm:ss");
      item.dValue = new Date(item.startTime).getTime() - new Date(this.lists[0].startTime).getTime()
      if (this.clearSpace(item.operationName) == "HTTPGET/dispatch" || this.clearSpace(item.operationName) == "HTTPGET:/customer" || this.clearSpace(item.operationName) == "HTTPGET" ) {
        item.color = "rgb(166, 128, 92)"
      } else if (this.clearSpace(item.operationName) == "SQLSELECT") {
        item.color = "rgb(245, 198, 192)"
      } else if (item.operationName == "/driver.DriverService/FindNearest") {
        item.color = "rgb(241, 216, 161)"
      } else if (item.operationName == "GetDriver") {
        item.color = "rgb(230, 145, 111)"
      } else if (this.clearSpace(item.operationName) == "HTTPGET:/route") {
        item.color = "rgb(109, 134, 196)"
      } else {
        item.color = "rgb(77, 171, 178)"
      }
      // item.operationName = 'frontend：' + item.operationName
    }

    let date = new Date(this.lists[1].startTime).getTime() - new Date(this.lists[0].startTime).getTime()
    console.log(date)


    console.log(this.lists)

  },

  methods: {
    // 处理数字小数点
    numDot (num) {
      if (!isNaN(num)) {
        return ((num + '').indexOf('.') != -1) ? num.toFixed(1) : num;
      }
    },
    // 去除空格
    clearSpace(str) {
       let newStr = str.replace(/\s+/g,"");
       return newStr
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  background: rgb(236, 236, 236);
  height: 46px;
  .menu-top {
    width: 340px;
    border-right: solid 1px rgb(226, 226, 226);
    font-weight: 600;
    height: 46px;
    line-height: 46px;
    padding: 0 10px;
    box-sizing: border-box;
  }
  .time {
    flex: 1;
    display: flex;
    align-items: center;
    height: 46px;
    line-height: 46px;
    .time-scale {
      flex: 1;
      font-size: 14px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-right: solid 1px rgb(226, 226, 226);
      span {
        padding: 0 5px;
      }
    }
  }
}
.bar-list {
  display: flex;
  align-items: center;
  line-height: 30px;
  height: 30px;
  font-size: 14px;
  .menu-bar {
    width: 340px;
    background: rgba(247, 247, 247, 1);
    border-right: solid 1px rgb(226, 226, 226);
    padding: 0 10px;
    box-sizing: border-box;
  }
  .rectangle-bar {
    flex: 1;
    line-height: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    overflow: hidden;
    transition: all 0.3s;
    .color-bar {
      background: royalblue;
      height: 10px;
      border-radius: 5px;
      position: relative;
      transition: all 0.3s;
      .bar-value {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        left: 100%;
        padding-left: 6px;
      }
      .bar-value-left {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: 100%;
        padding-right: 6px;
      }
    }
    .color1 {
      background: rgb(166, 128, 92);
    }
  }
  &:hover {
    .rectangle-bar {
      background: rgb(241, 241, 241);
    }
    .menu-bar {
      background: rgb(241, 241, 241);
    }
  }
}
</style>
