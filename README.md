# concession-kiosk-frontend
Frontend component for the concession kiosk demo app
```
oc new-app https://github.com/pieterdauds/concession-kiosk-frontend.git --name frontend -e COMPONENT_BACKEND_HOST=backend -e COMPONENT_BACKEND_PORT=8080
oc expose svc/frontend
oc get routes
```

# External Database for pushing data
```
oc new-app --template=mongodb-ephemeral
oc set env dc/backend MONGODB_URL=mongodb://<generated username>:<generated password>@mongodb/sampledb
```
