# Introduction 
The aim of this microservice is to be able to dynamicaly convert between units of many different types. The microservice takes in a http file containing the unit type, the starting unit, the ending unit and the data being converted and outputs that converted data as a double with its unit type

# Getting Started
#### Installation of Docker 
<https://docs.docker.com/engine/install/>

#### Installation of Dapr 
<https://docs.microsoft.com/en-us/dotnet/architecture/dapr-for-net-developers/getting-started>

#### Installation of UnitsNet
Enter line into terminal
> dotnet add package UnitsNet --version 4.99.0
> 
#### Installation of RestClient
Search RestClient in the extension tab

# Build and Run
Load up Docker

Enter line into terminal
> dapr run --app-id "unit-conversion" --app-port "5000" --dapr-grpc-port "50010" --dapr-http-port "5010" -- dotnet run

On the UnitConversionTest.http fIle click send request on the unit you want converting.

 
