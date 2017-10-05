# PrintEnv

Example Node.js application that simply returns the process environment as a JSON object. Use jq to view the output.

E.g.
curl printenv:8080 | jq -S

## From File 
set READ_FROM_FILE=/config/sample.properties

## Add Config Map
oc create configmap printenv-data --from-file=sample.properties
oc volumes dc/printenv --add -m /config -t configmap --configmap-name printenv-data


