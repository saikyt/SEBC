```
{
  "timestamp" : "2017-06-23T00:15:08.331Z",
  "clusters" : [ {
    "name" : "saikyt",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2944401408"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "294440140"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1626603520"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "273"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "master"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "admin"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "root"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-063495b363683a5acc8358b3eb2cddd0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-693c67f9a40d56b0aa97e3c7d8fc94f9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0035f854908a47bb6"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8c5243d0c334ead1f0b879c8b2d1a573",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0f687cde8330d3b2d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eqaic70xhzs0iopt6upyyik1s"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-063495b363683a5acc8358b3eb2cddd0",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bp3dm17pm1xip6afuidk3bctl"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "vtIv0nlJSxlRHqgziwRDPffqInzYQE"
          }, {
            "name" : "role_jceks_password",
            "value" : "am51r7gylnfjs5zriod46i205"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-063495b363683a5acc8358b3eb2cddd0",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9qg9ybs4zgdjrkhwyy27we92y"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a3bsezitg6i910ycxw105fj1i"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-8c5243d0c334ead1f0b879c8b2d1a573",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0f687cde8330d3b2d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e7oqdwwgzcjpux4fzue49q0hk"
          }, {
            "name" : "serverId",
            "value" : "3"
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
          "value" : "master"
        }, {
          "name" : "database_password",
          "value" : "admin"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "root"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-9804f4c61547a4626769e3b9c680a4f2"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-063495b363683a5acc8358b3eb2cddd0",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1v9tcklfklh596tisgzixqjlq"
          }, {
            "name" : "secret_key",
            "value" : "hKMs3DWl4XHr38T6ozvVVycJazWjwu"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-063495b363683a5acc8358b3eb2cddd0",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "91esj5tcg5m5e0dtebmw2ikpt"
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
            "value" : "master"
          }, {
            "name" : "oozie_database_password",
            "value" : "admin"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "root"
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
        "name" : "oozie-OOZIE_SERVER-063495b363683a5acc8358b3eb2cddd0",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e2w9l83j3vlbwg2zayxxr3ntx"
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
            "value" : "16"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "15703"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "17034"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "8"
          } ]
        } ],
        "items" : [ {
          "name" : "hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "k9RJq3xeG9edpmlGYD5qHRYWwDSSZp"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5nz6bh99arr4kov6s7vg8hb81"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1tnosraj2xzamqi78lkvdxgga"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-693c67f9a40d56b0aa97e3c7d8fc94f9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0035f854908a47bb6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9croqqpmunyns6ow6bkgtquju"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-8c5243d0c334ead1f0b879c8b2d1a573",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0f687cde8330d3b2d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4gum49uby5om8g805v6imhwj8"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d5ivp7okyy9yn3q3fnvqzpil7"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "59"
          }, {
            "name" : "role_jceks_password",
            "value" : "a1oszsuoqn52t7g1x6lopxygy"
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
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3219965132"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
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
            "value" : "/dfs/journalnode"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2944401408"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2944401408"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "jGPgYoM9fvRcQBy674M5qLTt7f8ngM"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "dfs_namenode_acls_enabled",
          "value" : "true"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "kPu1VVutzAlPRa0COiE5vSM1pRLPZM"
        }, {
          "name" : "hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "hdfs_sentry_sync_enable",
          "value" : "true"
        }, {
          "name" : "hdfs_sentry_sync_path_prefixes",
          "value" : "/user/hive/warehouse,/user/myunixuser"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "1UP7p22MVh9aRffGlh9qlStqvwl1F0"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "262u39ki2lf8hsfabvhl5ydmj"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-693c67f9a40d56b0aa97e3c7d8fc94f9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0035f854908a47bb6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "adyvs9g7055zwgfh96bqscj68"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-8c5243d0c334ead1f0b879c8b2d1a573",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0f687cde8330d3b2d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4nms0nv5il213xbkv0yup9a28"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "act4s2zy00xexa89117g2l8ru"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "75ljmgry6khtumolcdephehjh"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cgsmo55ejkbbiws2z7ejk0n0s"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f56adck06kq7naga5u742spzi"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-063495b363683a5acc8358b3eb2cddd0",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dozha81bbg3oqvs9wjemkef06"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "erqj7sgbgr0ssr995zdzn9ttu"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5oehp4mav8l4oxh81ec54h3r9"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-1b7802ec8aff64133215e0e9bb2d18d8",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0844d35b975a78486"
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
            "value" : "69"
          }, {
            "name" : "role_jceks_password",
            "value" : "61malc5x5nfjk0vnpnlir2r30"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
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
            "value" : "63"
          }, {
            "name" : "role_jceks_password",
            "value" : "4sktsodoznh3ky1r9h3uqqw0t"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-9804f4c61547a4626769e3b9c680a4f2",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "i-077b2925f6dc4df5e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cwai6rq84m4jcjk6jnbb0zwb6"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SENTRY_SERVER",
          "items" : [ {
            "name" : "sentry_server_java_heapsize",
            "value" : "268435456"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "master"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "admin"
        }, {
          "name" : "sentry_server_database_user",
          "value" : "root"
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,mylinuxuser,selector"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-063495b363683a5acc8358b3eb2cddd0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0341cd636ab3d88f6"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-8c5243d0c334ead1f0b879c8b2d1a573",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "i-0f687cde8330d3b2d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "amugzl7f7tbhq2wswenszdmdv"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0f687cde8330d3b2d",
    "ipAddress" : "172.31.42.54",
    "hostname" : "dn1",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0035f854908a47bb6",
    "ipAddress" : "172.31.35.171",
    "hostname" : "dn2",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0341cd636ab3d88f6",
    "ipAddress" : "172.31.35.135",
    "hostname" : "edgenode",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-077b2925f6dc4df5e",
    "ipAddress" : "172.31.44.60",
    "hostname" : "master",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0844d35b975a78486",
    "ipAddress" : "172.31.37.141",
    "hostname" : "snn",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-9804f4c61547a4626769e3b9c680a4f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e17954cffcd5538dce74b813f00a418d2d4efa9c6cf5d1e80ad11487845c9ec2",
    "pwSalt" : -6071307087970186398,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-063495b363683a5acc8358b3eb2cddd0",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "3afaac9deaaa518c8bd90048cd35df38093fce0b05d0e887313860c0265e7e64",
    "pwSalt" : 8568511675041169932,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-063495b363683a5acc8358b3eb2cddd0",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "11514975a54ddc9cee717017ba5f69db17eaa899c65f3ba7c8e4925b37099f96",
    "pwSalt" : 6600215706333512442,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-063495b363683a5acc8358b3eb2cddd0",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b253638c252f595f0891d65687cb56576385ab12932af56e790c2a66d748e301",
    "pwSalt" : 2941548819379422864,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-9804f4c61547a4626769e3b9c680a4f2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "38963dab1048820491103cf52972bf1b0324ea77de1800d1f648fbc5b60df2c5",
    "pwSalt" : -2995305541030105553,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "7c7decb999c6bfc001e939e5f839c9dad94c48b5102baaf2dc61f76ddf1e8ae2",
    "pwSalt" : 7828309864439038366,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "85f5bc8d5ac1fd56730f75314d0950bed5b97a8fc430938bb41c23833f112138",
    "pwSalt" : -4536051894894491973,
    "pwLogin" : true
  }, {
    "name" : "saikyt",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "afc45cb5b920841aeeeb93cd0bab9151736edaa1878669374ca9cfe95079ba5e",
    "pwSalt" : -8925332888388756973,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "master"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "admin"
        }, {
          "name" : "firehose_database_user",
          "value" : "root"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "master"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "admin"
        }, {
          "name" : "headlamp_database_user",
          "value" : "root"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-9804f4c61547a4626769e3b9c680a4f2",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "i-077b2925f6dc4df5e"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "b9bd1sthwxzpc3fin32ncvrty"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-063495b363683a5acc8358b3eb2cddd0",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0341cd636ab3d88f6"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "708o3sqxe12tjfr3kezn71gtz"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-063495b363683a5acc8358b3eb2cddd0",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0341cd636ab3d88f6"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a0h16ty6ty6mou0lymivlf3fl"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-063495b363683a5acc8358b3eb2cddd0",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0341cd636ab3d88f6"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "1aj553p1rolmrnxlhdudq3wiy"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-063495b363683a5acc8358b3eb2cddd0",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0341cd636ab3d88f6"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8o4vzmzn25e8dfs6uokmxhll7"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-9804f4c61547a4626769e3b9c680a4f2",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-077b2925f6dc4df5e"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f4bumclxvr2g8l783jg8sdt0f"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/26/2012 20:00"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA9AAEACkhBRE9PUC5DT00ADGNsb3VkZXJhLXNjbQAAAAFZSwYSAQAXABAgnGF02kkMrrQi8/paeuY0AAAAAQ=="
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@HADOOP.COM"
    }, {
      "name" : "KDC_HOST",
      "value" : "master"
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac"
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```
