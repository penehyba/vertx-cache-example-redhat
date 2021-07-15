https://appdev.openshift.io/docs/vertx-runtime.html#example-cache-vertx

# vertx-cache-example

This example demonstrates how to use a cache server from an Eclipse Vert.x application.

## Deployment

1. Be sure to be logged in to your OpenShift cluster, and you are in the right OpenShift project
2. Deploy the cache server using:
```bash
oc apply -f service.cache.yml
```
3. Deploy the example with:
```bash
mvn oc:deploy -Popenshift
```
4. Access the exposed route (`greeting-service`) - a HTML page to use the example is exposed.

## Integration tests

Run integrations test using:

```bash
mvn verify -Popenshift,openshift-it
```
