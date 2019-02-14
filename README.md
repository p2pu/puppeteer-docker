# Base docker image to use for front-end testing

## Usage

```bash
docker run --rm -it --volume `pwd`:/opt/app/ \
  --link learningcircles-db:postgres \
  --link learningcircles \
  -e DATABASE_URL=postgres://postgres:password@postgres/lc \
  p2pu/puppeteer-docker \
  sh -c "cd /opt/app/ && npm i --only=dev && npm test"
```
