# hillel-lesson-20

Я создал Access keys, s3://vdovenko-hillel-conduit-frontend и arn:aws:cloudfront::534931358663:distribution/E3H1WCRTJEJTOM

Файл env.list содержит AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_DEFAULT_REGION

Билд докер имеджа:
docker build -t conduit-fe ./project-frontend

Запуск контейнера:
docker run -it --env-file /Users/aqvila/env.list conduit-fe aws s3 sync ./build/ s3://vdovenko-hillel-conduit-frontend

https://d3mo11l7kdlcxv.cloudfront.net
