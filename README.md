# 准备环境
https://docs.docker.com/guides/jupyter/

```Dockerfile
FROM quay.io/jupyter/base-notebook
RUN pip install --no-cache-dir matplotlib scikit-learn
```

```bash
docker run -d --restart=always --name=notebook -p 8889:8888 localhost/my-jupyter start-notebook.py --NotebookApp.token='my-token'
```