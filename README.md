# Pandoc Service

## Build the Docker Image

```bash
git clone git@github.com:elmsln/Pandoc-Service.git
cd Pandoc-Service
docker build -t pandoc-service .
```

## Usage

```bash
docker run -it --rm -v $(pwd):/src pandoc-service <input-filename>.html -s -o <output-filename>.md
```

Example:

```bash
docker run -it --rm -v $(pwd):/src pandoc-service ./tests/pandochtmltest.html -s -o ./tmp/output.md
```

## FAAS Resources

What is function as a service?

- https://en.wikipedia.org/wiki/Function_as_a_service
- https://www.cloudflare.com/learning/serverless/glossary/function-as-a-service-faas/

Here are some similar projects of this type?

- https://github.com/heyMP/jsonnet-service
- https://github.com/heyMP/r-service
- https://github.com/heyMP/pdf-generator-service
