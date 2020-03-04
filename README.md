# Pandoc Service

## Build the Docker Image

```bash
git clone git@github.com:IST-440-Pandoc/Pandoc-Service.git
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