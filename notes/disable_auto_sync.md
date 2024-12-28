# Disabling Autosync

1. Disable Autosync on `bootstrap` inside of the main Gitops
2. Edit `ApplicationSet/tenants` on the openshift-gitops namespace to turn off autosync
   1. `oc patch applicationset tenants --type='merge' -p '{"spec": {"template": {"spec": {"syncPolicy": {"automated": {"selfHeal": false}}}}}}' -n openshift-gitops`
3. Disalbe Autosync on `composer-ai-config`
4. Then you should be able to disable autosync on any of the other composer items
