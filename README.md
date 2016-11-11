# docker-react-yarn

Make a react template app with yarn command 

```
docker run -it --rm -v $(pwd):/code smizy/nodejs sh
> /code # yarn init -y
> /code # yarn add --dev react-scripts
> /code # yarn add react react-dom
> /code # exit

# Run dev server
docker run -it --rm -v $(pwd):/code -p 3000:3000 smizy/nodejs yarn start  

# Run build
docker run --rm -v $(pwd):/code smizy/nodejs yarn build 

# Run built page
docker run --rm -v $(pwd):/code smizy/nodejs yarn add --dev http-server
docker run -it --rm -v $(pwd):/code -w /code/build -p 8080:8080 smizy/nodejs hs

```