FROM microsoft/dotnet:2.0.6-sdk-2.1.101-stretch
WORKDIR /app
 # caches restore result by copying csproj file separately
COPY BTCPayServer.Tests/BTCPayServer.Tests.csproj BTCPayServer.Tests/BTCPayServer.Tests.csproj
COPY BTCPayServer/BTCPayServer.csproj BTCPayServer/BTCPayServer.csproj

WORKDIR /app/BTCPayServer.Tests
RUN dotnet restore
# copies the rest of your code
COPY . ../.

ENTRYPOINT ["dotnet", "test"]
