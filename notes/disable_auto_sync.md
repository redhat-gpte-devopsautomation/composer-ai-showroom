# Disabling Autosync

1. Disable Autosync on `bootstrap` inside of the main Gitops
2. Edit `ApplicationSet/tenants` on the openshift-gitops namespace to turn off autosync
   1. `oc patch applicationset tenants --type='merge' -p '{"spec": {"template": {"spec": {"syncPolicy": {"automated": {"selfHeal": false}}}}}}' -n openshift-gitops`
3. Disable Autosync on `composer-ai-config`

AutoSync should be disabled for the items in the composer argo.

# Updating AppOfApps repo to a new tag.

Do the same steps as above, but for step 3 change the version of `composer-ai-config` to desired version.