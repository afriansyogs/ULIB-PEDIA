FROM oven/bun:1 as base

WORKDIR /app

COPY package.json bun.lockb ./

RUN bun install

COPY . .

RUN bunx prisma generate

EXPOSE 4000

CMD ["bun", "run", "dev"]