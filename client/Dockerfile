FROM node:20

WORKDIR /app
COPY . .

# Add this line before running the build
ENV PARCEL_WATCHER_FORCE_POLLING=true

ENV PARCEL_WORKERS=0
ENV PARCEL_WATCHER_BACKEND=fs
RUN npm install && npm run build

EXPOSE 1234

CMD ["npx", "parcel", "src/index.html", "--port", "1234", "--open"]