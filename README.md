# Travis Trigger

Simple Bash script to allow triggering a build on travis

## Dependencies

- docopt{,s}
- jq
- travis.rb

Example: 
```
travis-trigger \
  --pro \
  --request="$(jq -n '{config: {notifications: {email: true}}, message: "that message though"}')" \
  repo/slug master
```
