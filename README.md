# 准备环境
https://docs.docker.com/guides/jupyter/

```Dockerfile
FROM quay.io/jupyter/base-notebook
RUN pip install --no-cache-dir matplotlib scikit-learn
```

```bash
docker run -d --restart=always --net=host --name=notebook -e http_proxy=http://127.0.0.1:20171 -e https_proxy=http://127.0.0.1:20171  -p 8889:8888 localhost/my-jupyter start-notebook.py --NotebookApp.token='1234'
```


