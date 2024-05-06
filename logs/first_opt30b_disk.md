```bash
^C^C(flexgen) jupyter-yyk@node2:~/FlexGen$ python3 -m flexgen.flex_opt --model facebook/opt-30b --percent  0 0 100 0 100 0
<run_flexgen>: args.model: facebook/opt-30b
/home/jupyter-yyk/.conda/envs/flexgen/lib/python3.12/site-packages/huggingface_hub/file_download.py:1132: FutureWarning: `resume_download` is deprecated and will be removed in version 1.0.0. Downloads always resume when possible. If you want to force a new download, use `force_download=True`.
  warnings.warn(
model size: 55.803 GB, cache size: 2.789 GB, hidden size (prefill): 0.029 GB
init weight...
warmup - generate
benchmark - generate
/home/jupyter-yyk/.conda/envs/flexgen/lib/python3.12/site-packages/torch/distributed/distributed_c10d.py:347: UserWarning: torch.distributed.reduce_op is deprecated, please use torch.distributed.ReduceOp instead
  warnings.warn(
Outputs:
----------------------------------------------------------------------
0: Paris is the capital city of France and the most populous city in the country. It is the second largest city in the European Union after London. Paris is also the seat of the French government
----------------------------------------------------------------------
3: Paris is the capital city of France and the most populous city in the country. It is the second largest city in the European Union after London. Paris is also the seat of the French government
----------------------------------------------------------------------

TorchDevice: cuda:4
  cur_mem: 0.0079 GB,  peak_mem: 4.9482 GB
TorchDevice: cpu
  cur_mem: 0.0000 GB,  peak_mem: 0.0000 GB
model size: 55.803 GB   cache size: 2.789 GB    hidden size (p): 0.029 GB
peak gpu mem: 4.948 GB  projected: False
prefill latency: 13.782 s       prefill throughput: 148.596 token/s
decode latency: 355.462 s       decode throughput: 0.349 token/s
total latency: 369.244 s        total throughput: 0.347 token/s
```