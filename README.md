# CI detection fixture

AC 6 / open decision 1. GitHub Actions (build only, NO test) + a Jenkinsfile that DOES run tests. Precedence in the code is 'first MATCH across all readable configs', not 'first FILE' - so this reports required from the Jenkinsfile. If the spec says GitHub Actions wins outright and Jenkins is ignored, this is a real mismatch to raise.

Expected verdict line in the Octiq chat:

    Tests required - CI runs `npm test`   (source: Jenkinsfile)
