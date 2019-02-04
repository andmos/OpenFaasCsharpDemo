OpenFaaS CSharp Demo
===

Boilerplate for getting CSharp [OpenFaaS](https://github.com/openfaas/faas) function up and running.

Follow the [setup guide](https://docs.openfaas.com/deployment/docker-swarm/).

```bash
faas-cli login -u admin --password
faas-cli build -f csharp-helloworld.yml
faas-cli deploy -f csharp-helloworld.yml
echo "Hello you" | faas-cli invoke csharp-helloworld
curl http://127.0.0.1:8080/function/csharp-helloworld -d "Hello hello"
```
