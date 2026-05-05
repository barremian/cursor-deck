# Use nginx to serve the Freiburg deck
FROM nginx:alpine

# Copy the deck-specific nginx configuration
COPY ./build-with-cursor-freiburg/nginx.conf /etc/nginx/conf.d/default.conf

# Copy the static deck files
COPY ./build-with-cursor-freiburg/index.html /usr/share/nginx/html/index.html
COPY ./build-with-cursor-freiburg/theme.css /usr/share/nginx/html/theme.css
COPY ./build-with-cursor-freiburg/assets /usr/share/nginx/html/assets
COPY ./build-with-cursor-freiburg/brand /usr/share/nginx/html/brand

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
