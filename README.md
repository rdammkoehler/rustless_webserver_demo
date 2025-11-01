# Rustless

> I hijacked the codebase of JK Gunnick from his article https://jgunnink.substack.com/p/rustless-serverless-rust
> I'm experimenting with What's Possible!' and since I don't yet really know Rust, I needed a lift.
> JK, if we ever meet, I'll buy you some coffee or something. Thanks for kicking me off in this adventure!

A serverless web service

Everything is included to demo deploying to Cloud Run on GCP.

Related Blogpost explaining in more detail how all this works: [https://jgunnink.substack.com/p/rustless-serverless-rust](https://jgunnink.substack.com/p/rustless-serverless-rust)

## My Goal

So I wanted to see if I could accomplish a number of things... 

- [x] A service (or more than one) in Cloud Run using Rust
- [x] A CICD Pipeline in GCP connected to a GitHub repo

I have other thoughts and ideas. They may be done elsewhere, or I might tweak this repo.

- [ ] Learn Rust well enough to make some fun services with TDD
- [ ] Build the necessary GCP infrastructure around those services
- [ ] Integrate some security
- [ ] Put a React front-end in front of some services 
- [ ] Have some fun

### Why?

Only nerds will really understand.
[@Magnus Stahre](https://github.com/magnusstahre) put it best when he said something like "Because!" 


### More nutty ideas,

* What if you could plan Zork or Hunt the Wumpus on a web-page backed by a Rust implementation?

## Getting started

You can run this locally if you like by building the docker image and running it.

To build:

```
docker build . -t rustless
```

To run:

```
docker run --rm -p 8080:8080 rustless
```

## Deploying

You can deploy this by running:

```
gcloud builds submit .
```

This will kick off a cloubuild job and towards the end of the build output, you'll have a running service URL outputted in the log. It will
look something like:

```
https://rustless-3qqsqbdsuq-uc.a.run.app
```

## Contributing

Any ideas to improve or changes requested can be made via the repo's issues or pull request section and are welcome.
