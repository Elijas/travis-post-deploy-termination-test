Example of how to do additional tests after successful deployment

In travis.yml:
```
after_deploy:
  - if ! ADD_TEST_SCRIPT_HERE; then travis_terminate 1; fi
```

Proof that it works (the only diff being test failing/suceeding):
1. Fails as it should: https://travis-ci.com/Elijas/travis-ci-after-deploy-termination-test/builds/96418334
2. Succeeds as it should: https://travis-ci.com/Elijas/travis-ci-after-deploy-termination-test/builds/96418609
