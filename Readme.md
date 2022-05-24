PREP:
1. setup MPAS system with flux + landscaper
2. setup target system
3. configure objects (target, repocontext, etc.) for target system in MPAS
4. prepare a delivery ocm (with repo)
5. prepare an installation repo


DEMO:
1. ocm transport
2. show ocm internals of introspect-delivery
ocm get resources -c -o tree ghcr.io/vasu1124/ocm//github.com/vasu1124/introspect-delivery:0.0.x 
3. In MPAS repo, initiate workflow w/gh-action for new installation
branch: main
landscape repo: vasu1124/introspect-installation
prefix: landscape
landscape branch to create: staging
landscape branch for delivery: delivery
product source: ghcr.io/vasu1124/ocm//github.com/vasu1124/introspect-delivery
4. in installation repo, show the PR
5. fix and merge the PR
6. wait for GitOps to kick in

7. make a change in delivery repo (typically this should be automated)
8. make release-patch
9. show new ocm delivery version
ocm get resources -c -o tree ghcr.io/vasu1124/ocm//github.com/vasu1124/introspect-delivery:0.0.x 
10. In installation repo, initiate workflow w/gh-action for Import Product Version (on delivery branch)
11. Show the commits on delivery branch
12. In installation repo, initiate workflow w/gh-action for Upgrade Landscape (on target branch)
13. in installation repo, show the PR
14. fix and merge the PR
15. show the content for GitOps





