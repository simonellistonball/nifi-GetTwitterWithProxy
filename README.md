# nifi-GetTwitterWithProxy
Interim version of the Nifi GetTwitter processor with support for proxy settings.

## Build instructions

The build relies on a branch of the twitter bird client, which supports proxy and proxy authentication. See: https://github.com/simonellistonball/hbc/tree/AddProxyBasicAuth

To build this, first grab the branch at https://github.com/kutsal/hbc/tree/http-proxy-support and

    mvn install

This will populate your local cache with a snapshot build including the proxy support.

Then build this repo

    mvn clean package

This will result in nifi-GetTwitterWithProxy-nar/target/nifi-GetTwitterWithProxy-nar-0.0.1-SNAPSHOT.nar. Copy this to your nifi/lib directory, and you will have a new processor available called GetTwitterWithProxy.
