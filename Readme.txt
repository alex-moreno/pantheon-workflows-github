
**Starting**

Setup the next Github Secrets (Settings->Secrets->Actions->Add new repository secret)

1. PANTHEON_SSH_KEY
    Copy the contents of the secret file after ```ssh-keygen -f  id_rsa_pantheon_github -e -m pem > id_rsa_pantheon_github.pem```
2. PANTHEON_REPO
    Get this from your Pantheon dashboard site, in the button Connection Info.
3. PANTHEON_SITE_NAME
    For PANTHEON_SITE_NAME I used dev-build, which will be the multidev repository that this Github Action will be creating
4. KNOWN_HOSTS
    This can be simply empty, so we just don't get any errors
5. SSH_CONFIG
    Add this:
        ´´´
        Host *.drush.in
          StrictHostKeyChecking no
          ´´´

Note: The key added  id_rsa_pantheon_github
    cat id_rsa_pantheon_github
