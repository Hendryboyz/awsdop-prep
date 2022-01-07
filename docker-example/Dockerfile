FROM public.ecr.aws/docker/library/golang:1.16-alpine3.14 AS build
#Install git
RUN apk add --no-cache git
#Get the hello world package from a GitHub repository
RUN git clone https://go.googlesource.com/example
# Build the project and send the output to /bin/HelloWorld 
RUN cd example && ls -al && go build -o /bin/HelloWorld ./hello

FROM public.ecr.aws/docker/library/golang:1.16-alpine3.14
#Copy the build's output binary from the previous build container
COPY --from=build /bin/HelloWorld /bin/HelloWorld
ENTRYPOINT ["/bin/HelloWorld"]
