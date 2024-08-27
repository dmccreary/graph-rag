# Ollama

Ollama is a free open source tool that makes it easy to run large-language models on your local home consumer-grade GPUs with limited RAM.  Getting set up with Ollama is only a matter of running two UNIX shell commands:

## Ollama Setup

The following line downloads a UNIX install.sh shell script and runs it:

```sh
curl -fsSL https://ollama.com/install.sh | sh
```

```sh
ollama run llama3.1
```

You can also run other models like Microsoft's Phi3 Mini:

```sh
ollama run phi3
```

## Why is Ollama so Amazing?

Ollama's ability to run larger models on a GPU with limited memory, like my 12GB NVIDIA GeForce 2080 Ti GPU, is largely due to the following optimizations and techniques:

1.  **Quantization**: Ollama often uses techniques like 4-bit or 8-bit quantization, which reduce the precision of the model weights. This significantly decreases the memory footprint without a substantial loss in model performance, allowing larger models to fit into smaller GPU memory.

As of this writing, the default precision in Ollama is 4-bits.

2.  **Memory-Efficient Architectures**: Some models are designed with efficiency in mind, using architectures that require less memory per parameter or leveraging sparse computations that only activate a portion of the model at a time.

3.  **Layer-by-Layer Loading**: Ollama can load and unload model layers or parts of the model dynamically, processing one layer at a time instead of keeping the entire model in memory simultaneously. This is a form of model sharding, where only the active parts of the model are in memory.

4.  **Optimized Memory Management**: Advanced memory management techniques, such as swapping parts of the model in and out of GPU memory or using CPU RAM as an overflow buffer, help in running larger models. Although this might introduce some latency, it allows larger models to operate on smaller GPUs.

5.  **Custom Kernels**: Ollama might use custom GPU kernels optimized for the specific hardware, which can maximize the utilization of available memory and compute resources.

6.  **Efficient Batch Processing**: By processing smaller batches or even single tokens at a time, Ollama can reduce the amount of memory needed during inference, allowing for larger models to be loaded and processed.

These techniques enable Ollama to run models that are technically larger than what the raw memory capacity of the GPU would traditionally allow, albeit with some trade-offs in terms of speed or latency.