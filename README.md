# Introduction 
The aim of this microservice is to be able to dynamicaly convert between units of many different types. The microservice takes in a http file containing the unit type, the starting unit, the ending unit and the data being converted and outputs that converted data as a double with its unit type

# Getting Started
TODO: Guide users through getting your code up and running on their own system. In this section you can talk about:
1.	Installation of Docker <https://docs.docker.com/engine/install/>
2.	Installation of Dapr <https://docs.microsoft.com/en-us/dotnet/architecture/dapr-for-net-developers/getting-started>
3.	Installation of UnitsNet
> dotnet add package UnitsNet --version 4.99.0
4. Installation of RestClient

# Build and Run
Run the following line of code in the teminal:
> dapr run --app-id "unit-conversion" --app-port "5000" --dapr-grpc-port "50010" --dapr-http-port "5010" -- dotnet run

On the UnitConversionTest.http fIle click send request.

 
