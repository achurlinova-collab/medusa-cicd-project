FROM node:20-alpine

WORKDIR /app

RUN npm install -g pnpm@9

COPY package.json ./
RUN npm pkg delete packageManager

RUN pnpm install --no-frozen-lockfile

COPY . .

EXPOSE 8000

ENV NODE_ENV=production

CMD ["pnpm", "dev"]
