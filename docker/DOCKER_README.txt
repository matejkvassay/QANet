BUILD DOCKER IMAGE:
cd <QAnet project folder>/docker/
docker build -t qanet_demo -f ./Dockerfile .

RUN DOCKER DEMO SERVER:
cd <QANet project folder>
docker run -v `pwd`:/server/ --network="host" --name=qanet_demo_server qanet_demo
