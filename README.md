# Rust-LLm webapp
A chatbot webapp with backend and frontend made using only Rust, the webapp is designed with TailwindCSS and the model used is an open source language model downloaded from HuggingFace.

## Setup Instructions

### Hardware
The project is using CUDA acceleration for faster responses


### Installations:

```
rustup toolchain install nightly
rustup target add wasm32-unknown-unknown
cargo install trunk cargo-leptos
npm install -D tailwindcss
```
### Model
You'll also need to download a model (in GGML format) of your choice that is [supported by the Rustformers/llm Crate](https://huggingface.co/models?search=ggml).

Replace the value of the `MODEL_PATH` enviroment variable in the `.env` file with the path to the model file


### Run on your system 
1. run `npx tailwindcss -i ./input.css -o ./style/output.css --watch` in a terminal - this will build `style/output.css` and automatically rebuild when a change is detected in `input.css`
2. run `cargo leptos watch` in the project directory. 
3. In in your browser, navigate to [http://127.0.0.1:3000](http://127.0.0.1:3000)

## Model Used

[https://huggingface.co/davzoku/cria-llama2-7b-v1.3-GGML](https://huggingface.co/davzoku/cria-llama2-7b-v1.3-GGML)

