# mapp-connect-client-java
Mapp Connect Client Java

This SDK can be used by any application that wants to communicate with Mapp Connect. It wraps up JWT token generation part and all the HTTP communication details.

In order to use it, it's enough to include attached jar file as Java project dependency.

Example usage


Instantiate client and specify API URL, integration ID and API key

MappConnectClient mappConnectClient = new MappConnectClient("https://jamie.g.shortest-route.com/charon", "9c88b780-f470-4e64-a63b-a022f600859e",
                "WWbIbZmHxacRrmF4iQ1jHE3SdOZD7RUE");



Get list of prepared messages

Map<String, String> messages = mappConnectClient.getMessages();



Get list of groups

Map<String, String> groups = mappConnectClient.getGroups();



Send contact profile to be processed by Mapp Connect and saved by Engage

mappConnectClient.sendUser("{\"email\":\"test@xx.xx\"}");



Each operation can be triggered by sendXxxx method on the client, for now each of them expects the full JSON payload to be provided as an argument.
