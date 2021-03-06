# Introduction 
The aim of this microservice is to be able to dynamicaly convert between units of many different types. The microservice takes in a *.http* file containing the unit type, the starting unit, the ending unit and the data being converted.

# Getting Started
#### Installation of Docker 
![Docker](https://github.com/AlexanderAzzopardi/UnitConvertor/blob/main/Saved%20Pictures/DockerLogo.jfif)
> <https://docs.docker.com/engine/install/>

#### Installation of Dapr 
![Dapr](https://github.com/AlexanderAzzopardi/UnitConvertor/blob/main/Saved%20Pictures/DaprLogo.jfif)
> <https://docs.microsoft.com/en-us/dotnet/architecture/dapr-for-net-developers/getting-started>

# Build and Run

* Make sure that **Docker Kubernetes** is running.

* Enter line into terminal:
    > dapr run --app-id "unit-conversion" --app-port "5000" --dapr-grpc-port "50010" --dapr-http-port "5010" -- dotnet run

* On the *UnitConversionTest.http* fIle click send request on the unit you want converting.

# Creating a unit conversion file (.http)
The file below is an example of a unit conversion of type "Length" converting from metres to millimetres with the starting value of 56 metres.

    POST http://localhost:5010/v1.0/invoke/unit-conversion/method/convert HTTP/1.1
    content-type: application/json
    {
        "value": 56,
        "unitType": "Length",
        "unitStart": "m",
        "unitEnd": "mm"
    }
This will output a value of;
    > 56000mm

---

# Units
### Dimenstions
The Base Dimension which can be converted between are:
- Length
- Mass
- Time
- Current
- Temperature
- Amount
 -LuminousIntensity
 
### Abbreviations
The units that are able to be converted between are in the *abb.txt* file. As these may be hard to determine what each abbreviation means, their meanings can be found in the *type.txt* file.
