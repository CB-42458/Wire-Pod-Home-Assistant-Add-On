# Use the official Alpine Linux image as the base
FROM alpine:latest

# Install Avahi and its dependencies
RUN apk add --no-cache avahi

# Copy the Avahi configuration file into the container
COPY avahi-daemon.conf /etc/avahi/avahi-daemon.conf

# Expose the mDNS port
EXPOSE 5353/udp

# Start the Avahi daemon
CMD ["avahi-daemon", "--no-drop-root", "--daemonize"]
