FROM ghcr.io/kercre123/wire-pod:main

# Create the /data directory
RUN mkdir -p /data/chipper /data/vosk

# Move the existing directories to /data
RUN mv /chipper /data/chipper && mv /vosk /data/vosk

# Create symbolic links to the new locations
RUN ln -s /data/chipper /chipper && ln -s /data/vosk /vosk

# Ensure the application uses the new paths (if needed, add specific configuration here)

# Start the application (replace with the actual command to start your application)
CMD ["/bin/sh", "-c", "./chipper/start.sh"]