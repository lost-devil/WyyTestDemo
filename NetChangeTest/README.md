#工程目的
观察网络变化时，ConnectivityManager.CONNECTIVITY_ACTION广播接收到Intent中包含的参数，以log打印出来


# 结果（设备：三星note3，android5.0）

## 1、wifi下初始化
>06-15 23:39:17.277 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:39:17.277 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: WIFI[] - WIFI, state: CONNECTED/CONNECTED, reason: (unspecified), extra: "CodeMonkey", roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:39:17.277 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 1
06-15 23:39:17.287 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:39:17.287 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> "CodeMonkey"
06-15 23:39:17.287 2207-2207/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:39:17.287 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------

## 2、关掉wifi
>06-15 23:40:21.287 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: WIFI[] - WIFI, state: DISCONNECTED/DISCONNECTED, reason: (unspecified), extra: <unknown ssid>, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 1
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> <unknown ssid>
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest I/NetChange: noConnectivity ---> true
06-15 23:40:21.287 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------



## 3、打开wifi
>06-15 23:41:14.977 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: WIFI[] - WIFI, state: CONNECTED/CONNECTED, reason: (unspecified), extra: "CodeMonkey", roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 1
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> "CodeMonkey"
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:41:14.977 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------



## 4、关掉wifi自动切到mobile
>06-15 23:42:54.637 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: WIFI[] - WIFI, state: DISCONNECTED/DISCONNECTED, reason: (unspecified), extra: <unknown ssid>, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 1
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> <unknown ssid>
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest I/NetChange: noConnectivity ---> true
06-15 23:42:54.637 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: MOBILE[HSPA] - MOBILE, state: CONNECTED/CONNECTED, reason: (unspecified), extra: 3gnet, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 0
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> 3gnet
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:42:57.577 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------



## 5、打开wifi自动从mobile切到wifi
>06-15 23:44:24.987 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:44:24.987 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: MOBILE[HSPA] - MOBILE, state: DISCONNECTED/DISCONNECTED, reason: (unspecified), extra: 3gnet, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:44:24.987 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 0
06-15 23:44:24.987 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 100
06-15 23:44:24.987 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> 3gnet
06-15 23:44:24.987 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: WIFI[] - WIFI, state: CONNECTED/CONNECTED, reason: (unspecified), extra: "CodeMonkey", roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest I/NetChange: networkType ---> 1
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest I/NetChange: extraInfo ---> "CodeMonkey"
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:44:24.997 2207-2207/com.wyy.netchangetest D/NetChange: --------onReceive: end--------


## 6、mobile下初始化
>06-15 23:45:42.157 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: MOBILE[HSPA] - MOBILE, state: CONNECTED/CONNECTED, reason: (unspecified), extra: 3gnet, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest I/NetChange: networkType ---> 0
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest I/NetChange: extraInfo ---> 3gnet
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:45:42.157 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: end--------


## 7、关掉mobile
>06-15 23:46:09.767 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: MOBILE[HSPA] - MOBILE, state: DISCONNECTED/DISCONNECTED, reason: (unspecified), extra: 3gnet, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest I/NetChange: networkType ---> 0
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest I/NetChange: extraInfo ---> 3gnet
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest I/NetChange: noConnectivity ---> true
06-15 23:46:09.767 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: end--------


## 8、打开mobile
>06-15 23:46:53.657 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: begin--------
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest I/NetChange: networkInfo ---> [type: MOBILE[HSPA] - MOBILE, state: CONNECTED/CONNECTED, reason: (unspecified), extra: 3gnet, roaming: false, failover: false, isAvailable: true, isConnectedToProvisioningNetwork: false]
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest I/NetChange: networkType ---> 0
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest I/NetChange: inetCondition ---> 0
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest I/NetChange: extraInfo ---> 3gnet
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest I/NetChange: isDefault ---> true
06-15 23:46:53.657 16196-16196/com.wyy.netchangetest D/NetChange: --------onReceive: end--------
