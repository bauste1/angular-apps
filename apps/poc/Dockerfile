# build stage
FROM node:20-alpine AS build
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci

COPY . .

RUN npx nx run poc:build:production


# Stage 2: Serve the Angular application with NGINX
FROM --platform=linux/arm64 nginx


COPY --from=build /app/dist/apps/poc/browser /usr/share/nginx/html
# COPY ./nginx/default.conf /etc/nginx/conf.d/

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]