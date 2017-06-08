```
{
  "timestamp" : "2017-05-25T15:31:32.740Z",
  "clusters" : [ {
    "name" : "Cluster 1",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "407896064"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "35z7mme30zs7utpicfdiasgy4"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "407896064"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "407896064"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn,/mnt/resource/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3157157068"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "529530880"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn,/mnt/resource/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "407896064"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "407896064"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "9Jd269wNoN6EVrVVfDkmwimhsR5Win"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "h3WmQ6zYo5haSoZZTXE0TS4K8Gia27"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "2zR05nnNHkHdgtt4AjhhQX7Lpa9IxH"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-836e6c5869db075ce8d17ba568e621ee",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b5yu8fjlj662ka121b3u8j1ec"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-836e6c5869db075ce8d17ba568e621ee",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "34"
          }, {
            "name" : "role_jceks_password",
            "value" : "erxgcqgbcub4svpcjdbx8cn2k"
          } ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-836e6c5869db075ce8d17ba568e621ee",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "20gte8p18s8s5g8any5cbzagh"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "407896064"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "node_manager_java_heapsize",
            "value" : "407896064"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/mnt/resource/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/mnt/resource/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "2"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "407896064"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "1024"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "2"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "ohvYz3JASTwU9dQY5PTfuvVSWermUo"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-836e6c5869db075ce8d17ba568e621ee",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "rqwcjp9kbzz70mb9fqxewpoi"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "t52yv2t72t63zmog3thftyqu"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "32"
          }, {
            "name" : "role_jceks_password",
            "value" : "2auu9orrhgmtw7iwdw2wdy6dl"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "407896064"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "407896064"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "2"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "912680550"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "153"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "majednode1"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "8L7IL4Aj36"
        }, {
          "name" : "hive_metastore_database_port",
          "value" : "7432"
        }, {
          "name" : "hive_metastore_database_type",
          "value" : "postgresql"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-836e6c5869db075ce8d17ba568e621ee",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-836e6c5869db075ce8d17ba568e621ee",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bedespoxuadqkpytufsp5uhw3"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-836e6c5869db075ce8d17ba568e621ee",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6l3gx89wtmkhsgsp5vldqf53c"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "majednode1:7432"
          }, {
            "name" : "oozie_database_name",
            "value" : "oozie_oozie_server"
          }, {
            "name" : "oozie_database_password",
            "value" : "sNuFyT4TV0"
          }, {
            "name" : "oozie_database_type",
            "value" : "postgresql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie_oozie_server"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "407896064"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eyx6kryvcru6j6zwre5jcqyax"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "majednode1"
        }, {
          "name" : "database_password",
          "value" : "JBchmcSQfd"
        }, {
          "name" : "database_port",
          "value" : "7432"
        }, {
          "name" : "database_type",
          "value" : "postgresql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-836e6c5869db075ce8d17ba568e621ee"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-836e6c5869db075ce8d17ba568e621ee",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b9pcizwz2ryk8hk3gf3y7hzfr"
          }, {
            "name" : "secret_key",
            "value" : "jkOn6k8i64J8WVZSkJST8dZqqIVgog"
          } ]
        }
      } ],
      "displayName" : "Hue"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2",
    "ipAddress" : "10.0.1.5",
    "hostname" : "majednode1",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-836e6c5869db075ce8d17ba568e621ee",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e4b0789da75dda18717dd4f0f38c630c142cc42205e7eb3dbba6ee0f3dd7bc3a",
    "pwSalt" : 9214982911949467933,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-836e6c5869db075ce8d17ba568e621ee",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "dab884c00e099592b693fe2f12e084597ad675397431a30d222dcf4d0e5e3c31",
    "pwSalt" : 8576630451957798260,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-836e6c5869db075ce8d17ba568e621ee",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4bbb6801da1ed14e00622ca2a2d0ea87554f6ac4021aa6fd714da19c4845c239",
    "pwSalt" : 6108268664099786128,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-836e6c5869db075ce8d17ba568e621ee",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4bb4dc36d9f402d33efc61f96e0edd8683c9b6815d2b0d5dab380a36073e183e",
    "pwSalt" : 7893484260449359598,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "33c64f1991c474b9f78d36717c5d836c2e4e5b04311a89f51d0f1065c79827e1",
    "pwSalt" : 8569997843739313094,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.0",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170412-1249",
    "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "407896064"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "407896064"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "majednode1:7432"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "bpGTSQZ7Y3"
        }, {
          "name" : "headlamp_database_type",
          "value" : "postgresql"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "407896064"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "407896064"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-836e6c5869db075ce8d17ba568e621ee",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "60ot6n982jn7t0dokxokz6hlo"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-836e6c5869db075ce8d17ba568e621ee",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4cl8sw4vw5koxyqn0ik89f6uz"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-836e6c5869db075ce8d17ba568e621ee",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7j783f50uqz8iptntjjorixvd"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-836e6c5869db075ce8d17ba568e621ee",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bjw1f9qxdljqpbq159hsf0x3u"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-836e6c5869db075ce8d17ba568e621ee",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "71bec2ff-0267-4356-933c-f1760ec719d2"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eccyj9qa70c0hsajwrid3vafo"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 17:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```
