
```bash
# retrieves detailed information about a Docker image in JSON format
docker image inspect nginx:latest

# listing the layers that make up the image and their metadata
docker image history nginx:latest
```

- App binaries and dependencies
- Metadata about the image data and how to run the image
- Not a complete OS, no kernel, kernel module (e.g drivers)