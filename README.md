# Pandoc Service

## Build the Docker Image

```bash
git clone https://github.com/elmsln/Pandoc-Service.git
cd Pandoc-Service
docker build -t pandoc-service .
```

## Usage

Linux / Windows PowerShell:

```bash
docker run -it --rm -v "$(pwd):/src" pandoc-service <input-filename>.html -s -o <output-filename>.md
```

Linux / Windows PowerShell Example:

```bash
docker run -it --rm -v "$(pwd):/src" pandoc-service ./tests/pandochtmltest.html -s -o ./tmp/output.md
```

Windows Command Line:

```bash
docker run -it --rm -v "%cd%:/src" pandoc-service "<input-filename>.html" -s -o "<output-filename>.md"
```

Windows Command Line Example:

```bash
docker run -it --rm -v "%cd%:/src" pandoc-service "./tests/pandochtmltest.html" -s -o "./tmp/output.md"
```

Linux / Windows PowerShell convert and move file location:

```bash
docker run -it --rm -v "$(pwd):/src" pandoc-service <input-filename>.html -s -o <output-filename>.md | mv <output-filename> <new/file/location>
```

## FAAS Resources

What is function as a service?

- https://en.wikipedia.org/wiki/Function_as_a_service
- https://www.cloudflare.com/learning/serverless/glossary/function-as-a-service-faas/

