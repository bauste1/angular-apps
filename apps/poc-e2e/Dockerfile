FROM arm64v8/node:20-alpine AS build
WORKDIR /app
#COPY package.json package-lock.json ./
#RUN npm ci
#COPY . .
#RUN npx nx run poc-e2e:build:production

# Stage 2: Serve the Angular application with NGINX
#FROM arm64v8/nginx:1.27.0-alpine
#COPY --from=build /app/dist/apps/poc-e2e/browser /usr/share/nginx/html
#EXPOSE 8080
#CMD ["nginx", "-g", "daemon off;"]