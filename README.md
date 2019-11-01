# DS_lab9

~~~ 
rs0:SECONDARY> rs.config()
{
 "_id" : "rs0",
 "version" : 3,
 "protocolVersion" : NumberLong(1),
 "writeConcernMajorityJournalDefault" : true,
 "members" : [
  {
   "_id" : 0,
   "host" : "server1:27017",
   "arbiterOnly" : false,
   "buildIndexes" : true,
   "hidden" : false,
   "priority" : 1,
   "tags" : {
    
   },
   "slaveDelay" : NumberLong(0),
   "votes" : 1
  },
  {
   "_id" : 1,
   "host" : "server2:27017",
   "arbiterOnly" : false,
   "buildIndexes" : true,
   "hidden" : false,
   "priority" : 1,
   "tags" : {
    
   },
   "slaveDelay" : NumberLong(0),
   "votes" : 1
  },
  {
   "_id" : 2,
   "host" : "server3:27017",
   "arbiterOnly" : false,
   "buildIndexes" : true,
   "hidden" : false,
   "priority" : 1,
   "tags" : {
    
   },
   "slaveDelay" : NumberLong(0),
   "votes" : 1
  }
 ],
 "settings" : {
  "chainingAllowed" : true,
  "heartbeatIntervalMillis" : 2000,
  "heartbeatTimeoutSecs" : 10,
  "electionTimeoutMillis" : 10000,
  "catchUpTimeoutMillis" : -1,
  "catchUpTakeoverDelayMillis" : 30000,
  "getLastErrorModes" : {
   
  },
  "getLastErrorDefaults" : {
   "w" : 1,
   "wtimeout" : 0
  },
  "replicaSetId" : ObjectId("5dbc63b19dd0a805cc8ee611")
 }
}
rs0:SECONDARY>

rs0:SECONDARY> rs.status()
{
 "set" : "rs0",
 "date" : ISODate("2019-11-01T18:19:01.883Z"),
 "myState" : 2,
 "term" : NumberLong(2),
 "syncingTo" : "server3:27017",
 "syncSourceHost" : "server3:27017",
 "syncSourceId" : 2,
 "heartbeatIntervalMillis" : NumberLong(2000),
 "majorityVoteCount" : 2,
 "writeMajorityCount" : 2,
 "optimes" : {
  "lastCommittedOpTime" : {
   "ts" : Timestamp(1572632334, 1),
   "t" : NumberLong(2)
  },
  "lastCommittedWallTime" : ISODate("2019-11-01T18:18:54.038Z"),
  "readConcernMajorityOpTime" : {
   "ts" : Timestamp(1572632334, 1),
   "t" : NumberLong(2)
  },
  "readConcernMajorityWallTime" : ISODate("2019-11-01T18:18:54.038Z"),
  "appliedOpTime" : {
   "ts" : Timestamp(1572632334, 1),
   "t" : NumberLong(2)
  },
  "durableOpTime" : {
   "ts" : Timestamp(1572632334, 1),
   "t" : NumberLong(2)
  },
  "lastAppliedWallTime" : ISODate("2019-11-01T18:18:54.038Z"),
  "lastDurableWallTime" : ISODate("2019-11-01T18:18:54.038Z")
 },
 "lastStableRecoveryTimestamp" : Timestamp(1572632314, 1),
 "lastStableCheckpointTimestamp" : Timestamp(1572632314, 1),
 "members" : [
  {
   "_id" : 0,
   "name" : "server1:27017",
   "ip" : "172.31.81.76",
   "health" : 1,
   "state" : 2,
   "stateStr" : "SECONDARY",
   "uptime" : 388,
   "optime" : {
    "ts" : Timestamp(1572632334, 1),
    "t" : NumberLong(2)
   },
   "optimeDate" : ISODate("2019-11-01T18:18:54Z"),
   "syncingTo" : "server3:27017",
   "syncSourceHost" : "server3:27017",
   "syncSourceId" : 2,
   "infoMessage" : "",
   "configVersion" : 3,
   "self" : true,
   "lastHeartbeatMessage" : ""
  },
  {
   "_id" : 1,
   "name" : "server2:27017",
   "ip" : "172.31.87.201",
   "health" : 1,
   "state" : 1,
   "stateStr" : "PRIMARY",
   "uptime" : 387,
   "optime" : {
    "ts" : Timestamp(1572632334, 1),
    "t" : NumberLong(2)
   },
   "optimeDurable" : {
    "ts" : Timestamp(1572632334, 1),
    "t" : NumberLong(2)
   },
   "optimeDate" : ISODate("2019-11-01T18:18:54Z"),
   "optimeDurableDate" : ISODate("2019-11-01T18:18:54Z"),
   "lastHeartbeat" : ISODate("2019-11-01T18:19:01.480Z"),
   "lastHeartbeatRecv" : ISODate("2019-11-01T18:19:01.011Z"),
   "pingMs" : NumberLong(0),
   "lastHeartbeatMessage" : "",
   "syncingTo" : "",
   "syncSourceHost" : "",
   "syncSourceId" : -1,
   "infoMessage" : "",
   "electionTime" : Timestamp(1572627873, 1),
   "electionDate" : ISODate("2019-11-01T17:04:33Z"),
   "configVersion" : 3
  },
  {
   "_id" : 2,
   "name" : "server3:27017",
   "ip" : "172.31.81.171",
   "health" : 1,
   "state" : 2,
   "stateStr" : "SECONDARY",
   "uptime" : 387,
   "optime" : {
    "ts" : Timestamp(1572632334, 1),
    "t" : NumberLong(2)
   },
   "optimeDurable" : {
    "ts" : Timestamp(1572632334, 1),
    "t" : NumberLong(2)
   },
   "optimeDate" : ISODate("2019-11-01T18:18:54Z"),
   "optimeDurableDate" : ISODate("2019-11-01T18:18:54Z"),
   "lastHeartbeat" : ISODate("2019-11-01T18:19:01.480Z"),
   "lastHeartbeatRecv" : ISODate("2019-11-01T18:19:00.207Z"),
   "pingMs" : NumberLong(0),
   "lastHeartbeatMessage" : "",
   "syncingTo" : "server2:27017",
   "syncSourceHost" : "server2:27017",
   "syncSourceId" : 1,
   "infoMessage" : "",
   "configVersion" : 3
  }
 ],
 "ok" : 1,
 "$clusterTime" : {
  "clusterTime" : Timestamp(1572632334, 1),
  "signature" : {
   "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
   "keyId" : NumberLong(0)
  }
 },
 "operationTime" : Timestamp(1572632334, 1)
}
rs0:SECONDARY>
~~~


![](https://github.com/kolchanovavrn/DS_lab9/blob/master/2019-11-01%2021.39.43.jpg)
