# vr-gaussian

## 后端使用

从 [清华云盘链接](https://cloud.tsinghua.edu.cn/f/97d5941e9ddf4d64a577/) 中下载 `GaussianAssets.zip` 到项目根目录（与 `backend` 同目录），解压后运行：

```shell
./backend
```

运行后后端将运行在本地的 `12345` 端口。

## API

### GET /assets/{assetsName}

#### Request

```
GET http://localhost:12345/assets/bicycle
```

assetsName 属于：

```python
[
    "bicycle", "bonsai", "counter", "drjohnson", "flowers", "garden",
    "kitchen", "playroom", "room", "stump", "train", "treehill", "truck",
]
```

#### Response

HTTP 200 OK, body in json:

```json
{
    "pos": "string-base64",
    "pos_meta": "string-utf8",
    "shs": "string-base64",
    "shs_meta": "string-utf8",
    "chk": "string-base64",
    "chk_meta": "string-utf8",
    "col": "string-base64",
    "col_meta": "string-utf8",
    "oth": "string-base64",
    "oth_meta": "string-utf8",
    "asset": "string-base64",
    "asset_meta": "string-utf8"
}
```

#### Error

HTTP 404 Not Found, body in json:

```json
{
    "message": "msg"
}
```
