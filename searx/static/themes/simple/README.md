# Customising the SearXNG simple theme

## 1. Install dependencies

Run this command in the directory `searx/static/themes/simple`:

```bash
npm install
```

## 2. Modify CSS

Make your changes to `searx/static/themes/simple/src/less/definitions.less`

## 3. Compile sources

Run this command in the directory `searx/static/themes/simple`:

```bash
grunt
```

## 4. Create Docker image

Run this command in the SearXNG project root directory:

```bash
make docker.build
```

Then change the repository for the Docker image to something different:

```bash
docker image tag searxng/searxng:latest <your_username>/searxng:latest
```

where `<your_username>` is replaced with your own username (or organisation name).

Note that you can also run the two commands together by running:

```bash
make docker.build && docker image tag searxng/searxng:latest <your_username>/searxng:latest
```

## 5. (Optional) Push Docker image

If you have set up a remote container registry that you can upload to, push your Docker image to it by running:

```bash
docker push <your_username>/searxng:latest
```

For further information on `docker push`, see https://docs.docker.com/engine/reference/commandline/push/.
