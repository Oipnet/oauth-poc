FROM node:20-alpine AS node_upstream

FROM node_upstream AS base

ENV NODE_ENV=development

WORKDIR /srv/app
FROM base AS builder

COPY --link package.json package-lock.json ./
RUN npm install


FROM builder AS dev

EXPOSE 3000
EXPOSE 24678
ENV PORT 3000
ENV HOSTNAME localhost

COPY --from=builder /srv/app/node_modules /srv/app/node_modules

CMD [ "npm", "run", "dev" ]