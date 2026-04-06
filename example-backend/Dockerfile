FROM golang:1.16

WORKDIR /usr/src/app

EXPOSE 8080

COPY . .

RUN go build

ENV PORT=8080

ENV REQUEST_ORIGIN=http://localhost:5001

CMD ["./server"]