# Ollama Commands

These commands are useful for verifying an Ollama installation and working with local models.

## Check the installed version

```bash
ollama --version
```

## Start Ollama

### Using the systemd service

Check whether the service is running:

```bash
systemctl status ollama
```

If it is installed as a service but not running, start it with:

```bash
sudo systemctl start ollama
```

To enable it to start automatically at boot:

```bash
sudo systemctl enable ollama
```

### Starting the server manually

If you are not using the systemd service, you can start the server in a terminal:

```bash
ollama serve
```

Keep that terminal open, then open a second terminal to run a model.

If you see an **address already in use** error, another Ollama server may already be running. Check the service status, then try running a model directly.

## List downloaded models

```bash
ollama list
```

## Check running models

```bash
ollama ps
```

## Download a model

For example, to download the Qwen 2.5 3B model used in this project:

```bash
ollama pull qwen2.5:3b
```

## Run a model

Run Qwen 2.5 3B:

```bash
ollama run qwen2.5:3b
```

Or, for example, run Llama 3.2:

```bash
ollama run llama3.2
```

If the requested model is not already downloaded, Ollama may download it before running it.

[Back to the project overview](../README.md)
