# Assignment: Bind mounts

> Goal: Edit Code Running in Containers with Bind Mounts

- use a Jekyll "Static Site Generator" to start a local web server
- Don't have to be web developer: this is example of bridging the gap between local file access and apps running in containers
- source code is under `bindmount-sample-1`
- We edit files with editor on our host using native tools
- Container detects changes with host files and updates web server
- start container with `docker run -p 80:4000 -v $(pwd):/site bretfisher/jekyll-serve`
- Refresh our browser to see changes
	- Go to `localhost` to see the jekyll page
- Change the file in `_posts\` and refresh browser to see changes
