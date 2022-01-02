If you're storing docker files locally, you need to setup a registry on your device.

To do so, run the command:

docker-compose up -d

Now you can access localhost:5000

If you want to test pushing do the following command:

docker push localhost:5000/my-alpine

You can also pull or run it:

docker pull localhost:5000/my-alpine

docker run -it localhost:5000/my-alpine sh
