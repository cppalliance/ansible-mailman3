
## Single Sign On 

Relevant variables to enable single-sign-on, where another django website is the primary identity provider and the mailing lists are the relying party.

```
mailman3_django_config:
  socialaccount_providers:
    openid_connect:
      APPS:
        - provider_id: example21
          name: EXAMPLE21
          client_id: "____"
          secret: "____"
          settings:
            server_url: https://example21.org/.well-known/openid-configuration
            token_auth_method: client_secret_post
            oauth_pkce_enabled: true
  socialaccount_email_authentication: true
  socialaccount_email_authentication_auto_connect: true   # flip to true at Phase 5
  socialaccount_login_on_get: true
  socialaccount_only: true
  account_email_verification: "none"

mailman3_socialaccount_signup_stub: true
mailman3_socialaccount_auto_login_url: /accounts/oidc/example21/login/
