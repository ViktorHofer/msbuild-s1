FROM mcr.microsoft.com/dotnet/sdk:10.0 AS install
RUN dotnet tool install -g baronfel.binlog.mcp --version 0.0.13

FROM mcr.microsoft.com/dotnet/runtime:10.0
COPY --from=install /root/.dotnet/tools /root/.dotnet/tools
ENV PATH="$PATH:/root/.dotnet/tools"
ENTRYPOINT ["binlog.mcp"]
