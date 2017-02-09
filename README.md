# Ruby SAML

This is the OurHealth fork, based off of [onelogin/ruby-saml](https://github.com/onelogin/ruby-saml) (despite what GitHub says, this is no longer a fork of oacha/ruby-saml).

## Updating the Gem

A basic outline of the workflow going forward:

1. Check out this project
2. Run `bundle` inside the project directory
3. Run `rake` to confirm that the tests pass before you started
4. Set up one of the apps (`p3p` or `wellnest`) to use your local copy of the gem in the Gemfile (e.g. `gem 'ruby-saml', path: '/Users/ebrock/ruby-saml'`)
5. Make (and checkout a) branch in this project
6. Add https://github.com/onelogin/ruby-saml as a remote (e.g. `git remote add onelogin https://github.com/onelogin/ruby-saml`)
7. Set the branch to track the onelogin origin (`git branch -u onelogin/master`)
8. Merge in the changes from onelogin's version.
9. Run `rake` to confirm that the tests pass after you're done
10. Within the app that is pointing to the local copy of the gem, run `rspec ./spec/interactors/saml_sign_on_spec.rb`, to test that our fork still has all the changes needed.
11. Change your remote back to OurHealth (`git branch -u origin/master`)
12. Push up your changes
13. Put in a PR to get your changes reviewed
