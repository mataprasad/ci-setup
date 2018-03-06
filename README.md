https://blog.iamnguele.com/2018/02/21/continuous-delivery/

# dotnetcore-sample

Sample project allowing to get started with .NET Core. Was generated using the .NET Core CLI tools to illustrate a blog post written by Jean-Dominique Nguele and [available on blog.iamnguele.com](https://blog.iamnguele.com/2018/01/25/dot-net-core-cli-tools-10-minutes-api/). The commands below show how to quickly get started and must be ran from the root folder.

## Run the API

```
dotnet run --project DotNetCoreSampleApi
```

## Test the API

```
dotnet test DotNetCoreSampleApi.Tests
```

## Using Docker

### Build the API image

```
docker build -t aspnetapp DotNetCoreSampleApi
```

### Run the API image

```
docker run -d -p 8080:80 --name app aspnetapp
```

### Test the API using docker-compose

```
docker-compose -f docker-compose.unittests.yml run --rm unittests
```
