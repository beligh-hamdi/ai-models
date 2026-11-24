# ai


split -b 50M -d Qwen3-0.6B-Q4_0.gguf qwen3_

cat qwen3_* > Qwen3-0.6B-Q4_0.gguf

split -b 50M -d embeddinggemma-2-Q8_0.gguf embeddinggemma2_

cat embeddinggemma2_* > embeddinggemma-2-Q8_0.gguf

mkdir -p ~/.modeljars/cache/sha256/da/da2572f16c06133561ce56accaa822216f2391ef4d37fba427801cd6736417d4

curl -L "https://hf-mirror.com/ggml-org/Qwen3-0.6B-GGUF/resolve/main/Qwen3-0.6B-Q4_0.gguf" 
  -o ~/.modeljars/cache/sha256/da/da2572f16c06133561ce56accaa822216f2391ef4d37fba427801cd6736417d4/model.gguf


mkdir -p ~/.modeljars/cache/sha256/21/2188ac1deca4b77dffefd603c2776a9d76d9d74ec01841392982ebb840b09135

curl -L "https://hf-mirror.com/ggml-org/embeddinggemma-2-GGUF/resolve/bfcd298762cc34d0357ece5ebdd31791a3a374d8/embeddinggemma-2-Q8_0.gguf" 
  -o ~/.modeljars/cache/sha256/21/2188ac1deca4b77dffefd603c2776a9d76d9d74ec01841392982ebb840b09135/model.gguf


split -b 50M -d Inkling-2-Mini-UD-Q4_K_XL.gguf Inkling-2-Mini-UD-Q4_K_XL_

split -a 5 -b 5M Inkling-2-Mini-UD-Q4_K_XL.gguf Inkling-2-Mini-UD-Q4_K_XL_

cat Inkling-2-Mini-UD-Q4_K_XL_* > Inkling-2-Mini-UD-Q4_K_XL.gguf


```
# Modelfile
FROM  /Users/beligh/Downloads/ai/Qwen3-0.6B-Q4_0.gguf

# ollama create Qwen3-0.6B-Q4_0 -f Modelfile
```