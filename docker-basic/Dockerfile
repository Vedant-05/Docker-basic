FROM node:20-alpine

WORKDIR /app
# COPY . . mean first is copy erverything from source file to the /app folder for image
COPY . .

# this wont start the application it will just make the env for it 

RUN npm install
RUN npm run build
RUN npx prisma generate

EXPOSE 3000

# diff btween run and cmd run is for bootstraping the image and cmd is ran after image creation

CMD ["node","dist/index.js"]

