## setup installer

npm i -D ts-node typescript @types/node
npx tsc --init
npm i prisma @prisma/client
npx prisma init
npx prisma generate
npx prisma migrate dev --name init
npm run seed
npx prisma migrate reset

## Backend Install

npm i express body-parser cors dotenv helmet morgan

## for use runer Application Typescript

npm i -D rimraf concurrently nodemon @types/cors @types/express @types/morgan @types/node

## Um Id Fortzuführen in DB

SELECT setval(pg_get_serial_sequence('"Task"','id'), coalesce(max(id)+1, 1), false) FROM "Task";
