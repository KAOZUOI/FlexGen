```bash
^C^C(flexgen) jupyter-yyk@node2:~/FlexGen$ python3 -m flexgen.flex_opt --model facebook/opt-30b --percent 0 100 100 0 100 0
<run_flexgen>: args.model: facebook/opt-30b
/home/jupyter-yyk/.conda/envs/flexgen/lib/python3.12/site-packages/huggingface_hub/file_download.py:1132: FutureWarning: `resume_download` is deprecated and will be removed in version 1.0.0. Downloads always resume when possible. If you want to force a new download, use `force_download=True`.
  warnings.warn(
model size: 55.803 GB, cache size: 2.789 GB, hidden size (prefill): 0.029 GB
init weight...
Load the pre-trained pytorch weights of opt-30b from huggingface. The downloading and cpu loading can take dozens of minutes. If it seems to get stuck, you can monitor the progress by checking the memory usage of this process.
pytorch_model-00007-of-00007.bin: 100%|██████████████████████████████████████████████████████████████████████████████████████████████| 822M/822M [00:55<00:00, 14.7MB/s]
pytorch_model-00004-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.87G/9.87G [09:27<00:00, 17.4MB/s]
pytorch_model-00003-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.87G/9.87G [09:45<00:00, 16.9MB/s]
pytorch_model-00006-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.87G/9.87G [10:14<00:00, 16.1MB/s]
pytorch_model-00002-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.87G/9.87G [10:41<00:00, 15.4MB/s]
pytorch_model-00005-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.87G/9.87G [10:48<00:00, 15.2MB/s]
pytorch_model-00001-of-00007.bin: 100%|████████████████████████████████████████████████████████████████████████████████████████████| 9.79G/9.79G [10:53<00:00, 15.0MB/s]
Fetching 7 files: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7/7 [10:57<00:00, 93.88s/it]
Convert format: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7/7 [01:16<00:00, 10.95s/it]
warmup - generate                                                                                                                                                       
benchmark - generate
/home/jupyter-yyk/.conda/envs/flexgen/lib/python3.12/site-packages/torch/distributed/distributed_c10d.py:347: UserWarning: torch.distributed.reduce_op is deprecated, please use torch.distributed.ReduceOp instead
  warnings.warn(
/home/jupyter-yyk/FlexGen/flexgen/utils.py:132: UserWarning: TypedStorage is deprecated. It will be removed in the future and UntypedStorage will be the only storage class. This should only matter to you if you are using storages directly.  To access UntypedStorage directly, use tensor.untyped_storage() instead of tensor.storage()
  data_ptr = tensor.storage().data_ptr()
Outputs:
----------------------------------------------------------------------
0: Paris is the capital city of France and the most populous city in the country. It is the second largest city in the European Union after London. Paris is also the seat of the French government
----------------------------------------------------------------------
3: Paris is the capital city of France and the most populous city in the country. It is the second largest city in the European Union after London. Paris is also the seat of the French government
----------------------------------------------------------------------

TorchDevice: cuda:4
  cur_mem: 0.0079 GB,  peak_mem: 4.4567 GB
TorchDevice: cpu
  cur_mem: 56.5031 GB,  peak_mem: 0.0000 GB
model size: 55.803 GB   cache size: 2.789 GB    hidden size (p): 0.029 GB
peak gpu mem: 4.457 GB  projected: False
prefill latency: 5.519 s        prefill throughput: 371.068 token/s
decode latency: 153.959 s       decode throughput: 0.805 token/s
total latency: 159.478 s        total throughput: 0.803 token/s
```