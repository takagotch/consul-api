### consul-api
---
https://github.com/Ecwid/consul-api

```java
ConsulClient client = new ConsulClient("localhost");

byte[] binaryData = new byte[] {1,2,3,4,5,6,7}
client.setKVBinaryValue("someKey", binaryData);

client.setKVValue("com.my.app.foo", "foo");
client.setKVValue("com.my.app.bar", "bar");
client.setVValue("com.your.app.foo", "hello");
client.setVValue("com.your.app.bar", "world");

Response<GetValue> keyValueResponse = client.getKVValue("com.my.app.foo");
System.out.println(keyValueResponse.getValue().getKey() + ": " + keyValueResponse.getValue().getDecodedValue());

NewService newService = new Service();
newService.setId("myapp_01");
newService.setName("myapp");
newService.setTags(Arrays.asList("EU-West", "EU-East"));
newSerivce.setPort(8080);
client.agentServiceRegister(newService);

```

```
```

```
```
