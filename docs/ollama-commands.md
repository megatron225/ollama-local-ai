# Ollama Commands

These commands are useful for verifying an Ollama installation and working with local models.

## Check the installed version

```bash
ollama --version
```

## Check the service

```bash
systemctl status ollama
```

## List downloaded models

```bash
ollama list
```

## Check running models

```bash
ollama ps
```

## Download a model

```bash
ollama pull qwen2.5:3b
```

## Run a model

```bash
ollama run qwen2.5:3b
```

## Start Ollama

### If Ollama is installed as a system service

Check whether the service is running:

```bash
systemctl status ollama
```

If it is installed but not running, start it with:

```bash
sudo systemctl start ollama
```

To enable it to start automatically at boot:

```bash
sudo systemctl enable ollama
```

### Start the server manually

If you are not using the systemd service, you can start the server in a terminal:

```bash
ollama serve
```

Keep that terminal open, then open a second terminal to run a model.

If you see an **address already in use** error, another Ollama server may already be running. Check the service status, then try running a model directly.

## Run a model

For example, to run Llama 3.2:

```bash
ollama run llama3.2
```

To see which models you already have:

```bash
ollama list
```

If the requested model is not already downloaded, Ollama may download it before running it.
These examples use the 3B model from my project. A model can also be downloaded automatically when it is first run if it is not already present.

[Back to the project overview](../README.md)
