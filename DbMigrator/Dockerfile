FROM mcr.microsoft.com/dotnet/sdk:5.0
WORKDIR /build
COPY DbMigrator.csproj ./
RUN dotnet restore 
COPY . .
RUN dotnet publish -o /publish 
WORKDIR /publish 
CMD ["sh", "-c", "dotnet DbMigrator.dll \"${DB_CONNECTION}\""]
