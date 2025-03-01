# MNBVC_ARXIV_IMAGE2CAPTION

## 处理图文对
### 最终代码
```shell
python src/arxiv_main.py # 批量处理file.txt
# 代码效果，会将多种图片路径和写法提取出来、校验图片路径，读取图片，转为二进制写入parquet，一个arxiv一个parquet
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

### Other Notes
1. 文件存储路径需要定义，默认存储在 data/tex_source_parquet中
2. arxiv_main.py中需要传入file_list


## 处理公式和表格

### 最终代码
```shell
python src/arxiv_main_tableandequation.py # 批量处理file.txt
# 代码效果：会将每个arxiv的公式和图片提取出来，并尝试转为图片，形成latex公式与图文对
```


## 批量离散parquet合并为一个parquet
```shell
python src/concat_parquet.py # 批量处理parquet 文件
# 代码效果，会将n个parquet 合并为一个parquet 减少文件碎片
```



## TODO

更好的注释文件和README