**Browse or use curl on the endpoint ./api/v2/cm/deployment**
[root@aedg1-cdh58 centos]# curl -u 'g0dj4ck4l:cloudera' 'http://aedg1-cdh58:7180/api/v2/cm/deployment'
{
  "timestamp" : "2017-10-18T13:47:56.605Z",
  "clusters" : [ {
    "name" : "g0dj4ck4l",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "895483904"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "895483904"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2683672985"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "451"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "aedg1-cdh58.hadoop"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "Hive_tai2017"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9i8gh49u7vgf2t1odkylsoaia"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4xjg8mpzrgcixul5o86rxms2r"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "536870912"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-1ee19c348550e0f756c1a9a2bdc32e5c",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-05604cc2845096754"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8w3ypzaeusdfowm6pk6qtyfwh"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9uhn3btup4glfj1fezs2zxdu5"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "55mwwazmo8m1zqptgc5joq9kq"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "aedg1-cdh58.hadoop"
        }, {
          "name" : "database_password",
          "value" : "Hue_tai2017"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-ac29e5be4719ed8b16d43df6b58cc49b"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3zwyrcsjymc7uvvyxflhi4v9c"
          }, {
            "name" : "secret_key",
            "value" : "0ixDBKtKGvSCP3ahANIriEvzgBVBlD"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "aedg1-cdh58.hadoop"
          }, {
            "name" : "oozie_database_password",
            "value" : "Oozie_tai2017"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "536870912"
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
        "name" : "oozie-OOZIE_SERVER-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4h1qs78l88uxlapdarvy2f8vp"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3608"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3608"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "GqoPrqPshLKeRYuBPVyf403j2YhsOD"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3chvi65afr93zdc6xejo0z0m7"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1ee19c348550e0f756c1a9a2bdc32e5c",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-05604cc2845096754"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1vu614w9zxmh2pzgwit5wngon"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-76a3d830adc2122ab17b1d8faf1d93d5",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-056a7c287c6324ac8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "59v8v4o2flt55q27bfmec92nz"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a83258b25fa4f89e4f97cf5b171dc0b4",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0ce8251efed47f154"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4nhv6axpy76id93bfacm50xg"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "42"
          }, {
            "name" : "role_jceks_password",
            "value" : "abjlv5umjoyxe5ecn9xj3k6i"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "2947575398"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "nvoe6iSYEoms2s24Ojb2DwcoskokUc"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "GYX3NJJlkPwdjriNJ2xcW8JFCgdhwv"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "a7tGOdj3lwc24ptZ1MACVGiiwIxCEb"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-76a3d830adc2122ab17b1d8faf1d93d5",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-056a7c287c6324ac8"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1ee19c348550e0f756c1a9a2bdc32e5c",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-05604cc2845096754"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6zkfe5qvc36hu99y34gmraujs"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-76a3d830adc2122ab17b1d8faf1d93d5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-056a7c287c6324ac8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1qanccls1lb3ytc4ejpqi3b2g"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a83258b25fa4f89e4f97cf5b171dc0b4",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0ce8251efed47f154"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dfdc8nibib6ptg6bzav6t010"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-a83258b25fa4f89e4f97cf5b171dc0b4",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0ce8251efed47f154"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bfnipsir7hm83yr9ugqh6zi5b"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dhq32x66stjm3y11jdr3dgo94"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-HTTPFS-ac29e5be4719ed8b16d43df6b58cc49b",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-0d19289f381f0831d"
        },
        "config" : {
          "items" : [ {
            "name" : "httpfs_java_heapsize",
            "value" : "134217728"
          }, {
            "name" : "role_jceks_password",
            "value" : "3ebc9uoso1upbt6gvlalxdmw9"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-1ee19c348550e0f756c1a9a2bdc32e5c",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-05604cc2845096754"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4464sf4hxx7chv3h866eehgi"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-76a3d830adc2122ab17b1d8faf1d93d5",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-056a7c287c6324ac8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6aoy1qluel5theasee3sjlw10"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9m5cp8o938zckkof6l29auzng"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-a83258b25fa4f89e4f97cf5b171dc0b4",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0ce8251efed47f154"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "50"
          }, {
            "name" : "role_jceks_password",
            "value" : "7jl5l219hvmvntjqbkiuqo1o5"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-cd6a449af0842d1f2897823e5c643bc9",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0dce80b31dafa93dd"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "44"
          }, {
            "name" : "role_jceks_password",
            "value" : "3c3svuc59gpsgzcjlpi7hgjdy"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0d19289f381f0831d",
    "ipAddress" : "172.31.27.154",
    "hostname" : "aedg1-cdh58.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0dce80b31dafa93dd",
    "ipAddress" : "172.31.21.83",
    "hostname" : "amst1-cdh58.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0ce8251efed47f154",
    "ipAddress" : "172.31.18.8",
    "hostname" : "awrk1-cdh58.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-056a7c287c6324ac8",
    "ipAddress" : "172.31.20.76",
    "hostname" : "awrk2-cdh58.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-05604cc2845096754",
    "ipAddress" : "172.31.31.23",
    "hostname" : "awrk3-cdh58.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-ac29e5be4719ed8b16d43df6b58cc49b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "08111ab3a52031f47ebc0aa58aa8bae4013a850227596895897c3bd9c4983b95",
    "pwSalt" : 6486414127716743879,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-ac29e5be4719ed8b16d43df6b58cc49b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "cc1c53a26454149c564ea46d4953b9c4d10d29fd7c0904c7c002c3f77ada4a78",
    "pwSalt" : 8825478023812786484,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-ac29e5be4719ed8b16d43df6b58cc49b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "a08fcba17eaaef2c63f3e6fc3b32151b2b6842b887a102b2ad154ab6618884ae",
    "pwSalt" : -7664442055768938053,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-ac29e5be4719ed8b16d43df6b58cc49b",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "62da0eb02e60f093643fef19ef09548a6b14f9594e222fcb15febdb68451bb7c",
    "pwSalt" : -3624987321408474106,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "bea796ea4f53cdef48f929f7be41e6ff20268b1a7d995ec7b894283bcdae3b9e",
    "pwSalt" : 7436220338813880855,
    "pwLogin" : true
  }, {
    "name" : "g0dj4ck4l",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "563f4e5469a8eaf1086ceeaa58fdc1a514b45393787531596912ad492d8c12a8",
    "pwSalt" : -2552195806262136484,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "5c2057138bf365a4edec0e4ae093ee4851f980e20dc625d2913bed55b65071c9",
    "pwSalt" : 7544624859498021592,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1013",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "ALERTPUBLISHER",
        "items" : [ {
          "name" : "alert_heapsize",
          "value" : "134217728"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1677721600"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "536870912"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "aedg1-cdh58.hadoop"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "Rman_tai2017"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "895483904"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1782579200"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-ac29e5be4719ed8b16d43df6b58cc49b",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0d19289f381f0831d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dl64jo23y7y2lduuf1xmjygsv"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-ac29e5be4719ed8b16d43df6b58cc49b",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0d19289f381f0831d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "1slabhd9l0lqhy7ess29fjd6v"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-ac29e5be4719ed8b16d43df6b58cc49b",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0d19289f381f0831d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a5csko47xvuxbto8pqh8cl4hf"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-ac29e5be4719ed8b16d43df6b58cc49b",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0d19289f381f0831d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "c4h8ifjp4nlwnx8nrly0es8cj"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-ac29e5be4719ed8b16d43df6b58cc49b",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0d19289f381f0831d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eakpba1usiwjzau29lpqk2s5v"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/24/2012 18:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://aedg1-cdh58.hadoop/cdh5.8.3,https://archive.cloudera.com/cdh5/parcels/5.8.3,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
