# GrpcServiceNanoServer

An example project to show the issue with Grpc.Tools when running on .Net 9 and WindowsNanoServer. Created from the template in visual studio and adding docker support.

# Repo
From the root directory, build the project using:
`docker build -f .\GrpcServiceNanoServer\Dockerfile .`

This results in the following error as the protobuff targets are not available to generatre the classes from the .proto file:

`1>  C:\src\GrpcServiceNanoServer\Services\GreeterService.cs(6,35): error CS0246: The type or namespace name 'Greeter' could not be found (are you missing a using directive or an assembly reference?) [C:\src\GrpcServiceNanoServer\GrpcServiceNanoServer.csproj]
1>  C:\src\GrpcServiceNanoServer\Services\GreeterService.cs(14,51): error CS0246: The type or namespace name 'HelloRequest' could not be found (are you missing a using directive or an assembly reference?) [C:\src\GrpcServiceNanoServer\GrpcServiceNanoServer.csproj]
1>  C:\src\GrpcServiceNanoServer\Services\GreeterService.cs(14,30): error CS0246: The type or namespace name 'HelloReply' could not be found (are you missing a using directive or an assembly reference?) [C:\src\GrpcServiceNanoServer\GrpcServiceNanoServer.csproj]` 
