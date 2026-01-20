### What's changed in v0.1.0

* feat: initial commit (by @patrickleet)

* chore(deps): update unbounded-tech/workflow-simple-release action to v2.1.1 (#2) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat(deps): update helm release crossplane to v1.20.4 (#1) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* chore(deps): update unbounded-tech/workflows-crossplane action to v2.13.0 (#4) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat(deps): update helm release crossplane to v2 (#5) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat: fix the dumb ai stuff (by @patrickleet)

* fix: .m pc (by @patrickleet)

* feat: helm chart xrd (by @patrickleet)

* chore(deps): update unbounded-tech/workflow-vnext-tag action to v1.21.0 (#7) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* feat(deps): update crossplane-contrib/provider-helm docker tag to v1.0.6 (#6) (by @renovate[bot])

  Co-authored-by: renovate[bot] <29139614+renovate[bot]@users.noreply.github.com>

* fix: update e2e test with RBAC and separate namespace (by @patrickleet)

  - Add ClusterRoleBinding granting cluster-admin to crossplane-system SAs
  - Use Rapid channel instead of pinned version
  - Install to crossplane-test namespace to avoid conflicts with control plane
  - Remove unused import and custom values

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>

* fix: remove e2e tests - conflicts with control plane Crossplane (by @patrickleet)

  Crossplane XRD installs Crossplane itself, which creates cluster-scoped
  resources (ClusterRoles, CRDs) that conflict with the control plane
  Crossplane running in the e2e cluster.

  Render/validate/unit tests are sufficient for this XRD.

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>


