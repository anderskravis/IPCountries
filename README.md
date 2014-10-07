IPCountries
===========

A quick and easy JSON call to get the country name for IP addresses in a google sheet.

##Step 1:

In google sheets, navigate to Tools > Script Editor

Create a new script titled "ImportJSON.gs"

Next step is to copy the **ImportJSON** code by Trevor Lohrbeer (http://blog.fastfedora.com/projects/import-json). 

Save and Exit

##Step 2:

We're going to be making a call to http://freegeoip.net in order to return the country of an IP address
(You can also return a number of other data points to be listed below).

To make the call, copy the following formula into the cell you want the country name to reside in

*NOTE: Replace "IPCELL" with the cell reference to your IP Address*

```
=ImportJSON(CONCATENATE("http://freegeoip.net/json/",URLEncode(IPCELL)), "/country_name", "noHeaders")

```

That's it. The formula should return the country of the IP address if done correctly.



####Other Data:

The country name is one of a few data points you can gather from freegeoip. You can gather one of the others by simply changing the "/country_name" piece of the formula to one below (note that different IPs have varying level of traceability). 

- Country Code: */country_code*
- Region: */region_code*
- City: */city*
- Latitude: */latitude*
- Longitude: */longitude*










