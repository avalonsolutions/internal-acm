# internal-acm

This is a repo used to set config management for different services for an enterprise.
The master branch is protected and all changes must be approved by a member of the CISO team.
To suggest a change, create a new branch named policy/<new_change>.
Repoint the test anthos clusters to this branch for testing and then create a pull request to merge into the master branch for production deployment. 
All changes to the master branch are protected and have to be approved by a member of the CISO team.

## internalservices

This folder contains the policy tree for anthos clusters created via internal services.


When installing ACM for GKE clusters, add kube-system to the list of exemptable namespaces, and run *kubectl label namespace kube-system "admission.gatekeeper.sh/ignore=true"*