# k8s-sectemplate

This project aims to provide a mechanism by which a k8s cluster can be secured by automatically deploying needed policies to secure your kubernetes clusters at an operational level. This project will enable automatic deployemnt of 
- Pod security policies
- RBAC policies per namespace
- Network polcies

to provide needed isolation and security for pods running on separate namespaces. This reduces dependency on manual installation of yaml file everytime a namespace is created.The policies created per namespace will be controleld via the policies.yaml. ANything set in that file will be aplied to all newly/existing namespaces. If applied to existing namespaces , care need to be taken so that any existing pod communciation/capabilities are not broken. This might require installation of new psp/network/rbac policies to give appropriate pod permission.
