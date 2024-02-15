# Use the Nginx image from Docker Hub as a base
FROM nginx:alpine

# Copy the static files into the container
COPY index.html /usr/share/nginx/html/index.html
COPY style.css /usr/share/nginx/html/style.css

# Copy the entrypoint script into the container
COPY entrypoint.sh /entrypoint.sh

# Make the script executable
RUN chmod +x /entrypoint.sh

# Use the custom entrypoint
ENTRYPOINT ["/entrypoint.sh"]

# Start Nginx using the default command from the Nginx image
CMD ["nginx", "-g", "daemon off;"]
