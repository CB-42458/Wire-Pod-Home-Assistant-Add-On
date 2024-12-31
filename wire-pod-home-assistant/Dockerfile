FROM ghcr.io/kercre123/wire-pod:main

# Create the /data directory and subdirectories if they don't exist
RUN mkdir -p /data/chipper /data/vosk

# Create the /chipper and /vosk directories in the base image if they don't exist
RUN mkdir -p /chipper /vosk

# Check if /chipper exists and copy its contents to /data/chipper, then remove it
RUN [ -d /chipper ] && cp -r /chipper/* /data/chipper/ && rm -rf /chipper || echo "/chipper does not exist"

# Check if /vosk exists and copy its contents to /data/vosk, then remove it
RUN [ -d /vosk ] && cp -r /vosk/* /data/vosk/ && rm -rf /vosk || echo "/vosk does not exist"

# Create symbolic links to the new locations
RUN ln -s /data/chipper /chipper && ln -s /data/vosk /vosk

# Start the application (replace with the actual command to start your application)
CMD ["/bin/sh", "-c", "/chipper/start.sh"]
