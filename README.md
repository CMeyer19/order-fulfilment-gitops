# Order Fulfilment: GitOps

Deployment configuration for [order-fulfilment](https://github.com/cmeyer19/order-fulfilment), synced to a k3s cluster by **Argo CD**.

> 🚧 In progress.

- `charts/`: Helm charts for each service
- `apps/`: Argo CD Applications
- `platform/`: cluster add-ons (KEDA, CloudNativePG, MongoDB and RabbitMQ operators, Keycloak)

CI in the app repo builds images and commits new image tags here; Argo CD syncs the cluster. Application code and deployment config change at different times, so they live in separate repos.
