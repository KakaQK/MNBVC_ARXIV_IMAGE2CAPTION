# MNBVC_ARXIV_IMAGE2CAPTION


## 最终代码
```shell
python src/arxiv_main.py # 批量处理file.txt
```
```python
# 主要传入参数
parser.add_argument("--input_file", "-i", type=str, default="list.txt", help="Input file")
parser.add_argument("--workers_num", "-w", type=int, default=2, help="multi process workers num")
parser.add_argument("--output_dir", "-o", type=str, default=r"data_output/data-image-parquet", help="Output directory")
parser.add_argument("--log_dir", "-l", type=str, default="logs", help="Log path")

# 处理单个文件的函数
process_list_of_arxiv_files(file_list: List)
```

## Other Notes
1. 文件存储路径需要定义，默认存储在 data/tex_source_parquet中
2. arxiv_main.py中需要传入file_list

## TODO

更好的注释文件和README