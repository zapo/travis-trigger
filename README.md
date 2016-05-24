# Travis Trigger

Simple Bash script to allow triggering a build on travis

## Dependencies

- docopt{,s}
- jq
- travis.rb

Example: 
```
travis login && \
travis-trigger \
  --request="$(jq -n '{config: {notifications: {email: true}}, message: "that message though"}')" \
  repo/slug master
```
