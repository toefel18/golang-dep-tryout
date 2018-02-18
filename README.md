# golang-dep-tryout

init the project

    dep init   

add dependencies

    dep ensure -add github.com/foo/bar github.com/baz/quux


remove unusued dependencies & install required

    dep ensure
    
See [daily-dep documentation](https://golang.github.io/dep/docs/daily-dep.html)


Here are the key takeaways from that guide:

    dep ensure -update is the preferred way to update dependencies, though it's less effective for projects that don't publish semver releases.
    dep ensure -add is usually the easiest way to introduce new dependencies, though it's not the only one. To add more than one at a time, you'll need to use multiple arguments, not multiple invocations - and make sure to add real import statements for the projects after the command completes!
    If you ever make a manual change in Gopkg.toml, it's best to run dep ensure to make sure everything's in sync.
    dep ensure is almost never the wrong thing to run; if you're not sure what's going on, running it will bring you back to safety ("the nearest lilypad"), or fail informatively.
