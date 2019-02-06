This is a really simple python dev environment for simple flask apps and such. It could probably do a lot more but so far my intention is just small projects and tools.

# Usage

clone the repo, add your app or make an empty space for one... then enjoy:

```
git clone git@github.com:gNerdLabs/pythonDevStack.git newEnv
cd newEnv
```

`newEnv` is whatever you would like to call it.

personally I would `rm -rf .git` and only track the contents of the `./app` dir you are about to create.

using an existing app:

```
git clone git@github.com:something/existingApp.git app
```

or just start fresh:

```
mkdir app
cd app
echo "# my new app thing" >> README.md
git init
git add README.md
git commit -m "first commit"
etc ...
```

then start it up!

```
docker-compose up
```

it should pull all the images from dockerhub and start up easy

connect in a zsh shell:

```
docker exec -it newEnv_server_1 zsh
```

note that your folder name will dictate the container name. use `docker ps` to list them and get the appropriate name if you dont know it. 

your zsh history will be accessible in the `shared` dir. will also persist between rebuilds this way.

you can add your ssh keys in `./shared/ssh` and your aws cli config files in `./shared/aws` if you like. You can also generate them from within the container and they will persist here. 